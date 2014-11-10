---
layout: detailed-guidance
title: User stories for web operations
subtitle: A useful starting point when understanding the scope of infrastructure work
type: guide
status: draft
audience:
  primary: service-managers, delivery-managers, web-ops
  secondary: tech-archs, delivery-managers, developers
category: operations
breadcrumbs:
  -
    title: Home
    url: /service-manual
  -
    title: Operations
    url: /service-manual/operations
---

This document outlines the typical scope of infrastructure and web operations
(sometimes erroneously referred to as hosting) work on a large service
redesign project.

The sample list of user stories provided is not intended to be a complete list of
all areas of interest nor are you likely to need to do all of this for every service.
The idea is for this list to be a good starting place from where to you can write
additional stories, delete ones you do not require and split stories into smaller
ones. Importantly you also need to provide your own acceptance criteria
specific to the needs of your service.

Remember these stories are [a placeholder for a conversation](/service-manual/agile/writing-user-stories#promise-of-a-conversation).
For some contexts, that conversation will be 'this does not apply to my
service' -- that is fine. But there will almost certainly be other stories not
listed here which do apply.

本文概述了基礎設施和網路營運（有時誤稱為主機託管）上重新設計服務的大型專案工作的典型範圍。 

以下所提供的使用者故事範例清單並不是所有領域的完整使用者故事清單，也不是每個服務都需要以下所列全部的使用者故事清單。我們的想法是這個清單是個很好的起點，你可以寫更多的故事、刪除那些你不需要的故事和將故事分離成較小的故事。重要的是你需對要針對你的服務的需求，提供自己的驗收標準。 

請記住這些故事是[對話的樣式(a placeholder for a conversation)](/service-manual/agile/writing-user-stories#promise-of-a-conversation)。在一些脈絡下，該對話將是'這並不適用於我的服務' - 也沒關係。但幾乎可以肯定的是有其他未列出故事適用。 

## 問題 The problem

An issue we have observed on a number of projects is a lack of understanding
early on in a project about the work required to run a large online
service. Often this is placed under  _hosting_ and is investigated too late
in the process.

我們在一些専案中發現了一個問題，那就是對於執行一個大型的線上即時服務所需的工作，在専案的初期缺乏認識。通常這被歸類為 _主機託管(hosting)_ ，在過程中才被深入探討為時已晚。 

## 目標讀者 Intended audience

The hosting of a complex and sensitive software application requires a team
of people with specialist skills to design, setup and operate. Because this
work is generally not user facing and can be highly technical it is sometimes
easy to leave until later -- with potentially dire consequences for launching
safely and on time.

複雜而敏感的應用軟體的主機維運是需要由各種專業技能人才所組成的團隊來設計、安裝和操作。由於這種工作通常不需要面對使用者而且可以是高度技術性的工作，有時候容易被保留，直到 -- 對於安全準時上線具有潛在嚴重影響時。

### 服務經理 Service managers
Does your team have people who deeply understand this topic? If you are not an
expert then it is important to involve people permanently in the team
who are. They can explain the technical trade offs and decisions which may
affect your service.

您的團隊是否有人深刻瞭解這個主題？如果你不是這方面的專家，那麼團隊中需要有這方面的専家永久參與是非常重要的。他們可以解釋可能會影響您的服務的技術權衡和決定。

### 交付經理 Delivery managers
As well as understanding the potentially large scope of work, many of the areas
discussed here have lead times associated with third parties. The earlier
stories related to these topics are brought into project backlogs the sooner
estimates can be made and deadlines understood.

除了了解工作的潛在大範圍之外，這裡所討論的許多領域的完成時間都與第三方有關。與這些主題相關的故事愈早被帶進専案待處理項目清單中 (project backlog)，則時程可以愈早被估計以及理解它的期限。 

## 故事 Stories
The following stories are intended to provide a starting point for any project,
rather than be a complete set. Individual projects would be expected to take
and modify stories as needed and importantly to apply their own acceptance
criteria specific to their requirements.

下列的故事，旨在為任何専案提供一個起點，而不是一個完整的故事集合。個別専案可以使用這些故事並根據需要進行修改，重要的是針對他們的需求採用他們自己的驗收標準。 

The majority of these stories are from the point of view of developers, web
operations engineers and the responsible service manager. Although not ideal,
for this particular technical topic this works reasonably well. Feel free
to change the focus when using them in your backlog.

大多數這些故事都是從開發者、網路維運工程師和負責該服務的服務經理的觀點來編寫。雖然不盡理想，但對於這個特殊的技術主題來說這還算不錯。當你使用它們作為你的待處理項目清單時，你可以隨意修改。 

### 流程  Process

*開發流程 Development process*  
As a developer working on the service  
So that we can ensure a high level of quality  
And so we can maximise the integrity of the source code  
I want a well documented and understood development process

作為一名服務的開發人員 
為了達到，保證高水準的品質  
以及，最大化程式碼的完整性 
我想要一個記錄完整並易於了解的開發流程

*非工作時間的支援 Out-of-hours support*  
As the service manager responsible for the service  
So that we can ensure a suitable level of availability and integrity  
I want to understand the requirement for Out-of-hours support
 
作為一名對服務負責的服務經理 
為了達到，確保可用性和完整性的適當水準
我想要了解非工作時間的支援的需求 

*災害恢復 Disaster recovery*  
As the service manager responsible for the service  
So that in the event of a disaster everyone doesn't panic and make things up  
I want a clear disaster recovery plan in place to deal with different types of catastrophic event

作為對服務負責的服務經理
為了達到，在災難事件中，每個人不會慌亂並且克服它
我想要明確的災難恢復計劃被制定完成，以應付不同類型的災難性事件

*釋放過程 Release process*  
As the service manager responsible for the service  
So that the service can be changed on a very frequent basis  
And so that changes do not cause problems for users  
I want a well documented and understood release process

作為對服務負責的服務經理 
為了達到，該服務可以非常頻繁地被修改 
而且這樣的變化不會引起使用者的問題  
我想要一個記錄完整並易於了解的釋出或發佈流程 

*安全對策 Security response*  
As the service manager responsible for the service  
So that security incidents are handled with extra care  
And so that the service meets its wider Government obligation to GovCert  
I want a well documented and understood security incident process

作為對服務負責的服務經理
為了達到，安全事故被特別小心處理  
並且該服務滿足GovCert更廣泛的政府責任   
我想要一個記錄完整並易於了解的安全事故處理流程 

*服務台 Helpdesk*  
As the service manager responsible for the service  
So that communication with users is done in a joined up way  
I want a central helpdesk function to deal with events, incidents and requests

作為對服務負責的服務經理
為了達到，與使用者的溝通，將以聯合的方式完成   
我想要一個集中式的服務支援功能來處理事件，事故和要求

*需求管理 Request Management*  
As the service manager responsible for the service  
So that questions from users can be dealt with efficiently  
I want a clear information request management policy

作為對服務負責的服務經理
為了達到，由使用者提出的問題，可以有效地處理   
我想要一個明確的資訊要求管理政策 

*事件管理 Event Management*  
As the service manager responsible for the service  
So that likely events that could affect the running of the service can be dealt with smoothly  
I want a clear event management policy

作為對服務負責的服務經理
為了達到，可能影響服務的運作的事件，有可能順利地被處理   
我想要一個明確的事件管理政策 

*事故管理 Incident Management*  
As the service manager responsible for the service  
So that problems that arise with that service can be dealt with efficiently  
I want a clear incident management policy

作為對服務負責的服務經理
為了達到，由該服務發生的問題可以有效地被處理   
我想要一個明確的明確的事故管理政策

*操作手冊 Operations manual*  
As the service manager responsible for the service  
So that information about the running of the service is not kept in individuals’ heads  
And so information is readily available to people running the service  
I want a single place to store content for a service operations manual

作為對服務負責的服務經理
為了達到，關於執行該服務的資訊不會保存在個人的心中
並且該資訊可以隨時地供執行該服務的人使用   
我想要有一個單一的地方來存儲的服務操作手冊的內容 

### 共享服務 Shared service

*程式碼託管服務 Source code hosting*  
As a developer working on the service  
So we have somewhere to securely store our source code  
I want access to a central source code hosting service or repository
 
作為服務的開發人員
為了達到，能有地方安全地存儲我們的程式碼 
我想獲得一個集中的程式碼託管服務或資料庫 
 
*持續整合 Continuous Integration*  
As a developer working on the service  
So we can ensure a high level of quality in the code  
And so we can minimise the time needed for regression testings  
I want a Continuous Integration environment which automatically runs tests against every commit

作為服務的開發人員
為了達到，保證程式碼的高品質 
並且，可以減少進行回歸測試的時間 
我想要一個持續整合的環境，它可以在每次遞交程式碼時自動執行測試 

*外部DNS External DNS*  
As a web operations engineer  
So that visitors to the service don't need to remember an IP address that will change  
I want a process and supplier relationship to manage external DNS addresses

作為一個網站營運工程師 
為了達到，讓訪客進入該服務時，不需要記住常常變動的 IP 位址 
我想要有一個流程以及供應商關係來管理外部DNS地址 

### 政策 Policy

*程式碼的機密程度 Sensitivity of source code*  
As a developer working on the service  
So that I understand the controls that need to be in place  
And so that I know who and how I may share it  
I want a clear policy around the sensitivity of source code

作為一名服務的開發人員 
為了達到，明白那些管制必需完備
並且，知道可以跟誰分享以及如何分享程式碼 
我想要關於程式碼機密性的明確政策 

*第三方程式碼 Third party code*  
As a developer working on the service  
I want a clear policy around use of third party source code libraries  
So that I do not introduce unknown security problems

作為一名服務的開發人員  
我想要關於第三方程式碼函式庫使用上的明確政策 
因此，不會遇到未知的安全問題 

*變更評估 Change evaluation*  
As the service manager responsible for the service  
So that I can release changes to production quickly  
And so that we can meet our obligation to the Digital by Default Service Standard  
I want a documented process for evaluating and deciding on a change to the production service

作為對服務負責的服務經理  
為了達到，可以迅速將變更發行到正式環境 
以及，可以滿足我們Digital by Default Service的義務 
我想要記錄完整的，針對變更的服務釋出到正式環境的評估以及決定的流程 

*存取控制 Access control*  
As the service manager responsible for the service  
So that the confidentiality, integrity and availability of the service isn't compromised  
And so that suitable technical controls can be put in place to enforce it  
I want a clear policy on who has access to what on the production system

作為對服務負責的服務經理  
為了達到，服務的保密性、完整性和可用性不受損害 
並讓合適的技術控制可以到位，以便於執行 
我想要誰可以存取正式環境以及什麼可以被存取的的明確政策 

*職能分工 Separation of duties*  
As the service manager responsible for the service  
So that we can ensure the service has enough people in the right roles  
I want to understand any required separation of duties (whether driven by legislation or security concerns)

作為對服務負責的服務經理  
為了達到，確保服務有足夠多的工作人員並且處於正確的角色 
我想要了解任何必需的職能分工（不論是因為法律規定或安全問題而產生的） 

*許可 Clearances*  
As the service manager responsible for the service  
So that security clearances can be arranged early in the project to avoid access restrictions later on  
I want to know what level of clearances are required for different roles (including third parties)

作為對服務負責的服務經理  
為了達到，安全許可可以在専案中及早被安排，以避免日後的存取限制 
我想知道不同的角色需要什麼程度的安全許可（包括第三方） 

*發布開源碼 Releasing open source*  
As a developer working on the service  
So that I do not introduce unknown security problems  
And so that we can meet our obligation to the Digital by Default Service Standard  
I want a clear policy around releasing code as open source

作為一名服務的開發人員 
為了達到，不會遇到未知的安全問題
並且，滿足我們Digital by Default Service的義務 
我想要一個針對開源程式碼釋出的明確政策

### Design 設計

*政府網路 Government networks*  
As a technical architect  
So that the right suppliers are contracted  
And so that long lead times are factored into the project plan early  
I want to know whether the service requires access to a Government network like the PSN or GSI

作為一個技術架構師
為了達到，與適當的供應商簽約 
以及，長交付周期可以及早被納入専案計劃 
我想要知道這個服務是否需要存取政府網路，如PSN或GSI 

*多基礎設施供應商 Multiple infrastructure providers*  
As the service manager for this service  
So that I understand the intended availability constraints  
I want to know whether multiple suppliers of Infrastructure are required

作為這個服務的服務經理 
為了達到，明白預期的可用性限制 
我想知道是否需要多個基礎設施的供應商 

*容量規劃 Capacity planning*  
As a web operations engineer  
So that we can estimate the number and size of infrastructure components (instances, firewalls, load balancers etc.)  
And so that resource based costs can be estimated  
I want to carry out some capacity planning activities

作為一個網站營運工程師 
為了達到，可以估算基礎設施組件（實例、防火牆、負載均衡器等）的數量和大小 
以及，資源成本可以被估計 
我想要展開一些容量規劃的活動 

*網路架構 Network architecture*  
As a technical architect  
So that I can build out a production environment to an agreed specification  
I want a network architecture design

作為一個技術架構師
為了達到，可以建立符合規格的正式環境 
我想要網路架構設計 

### Components 組件 

*Web伺服器 Web servers*  
As a web operations engineer working on the service  
So that we can serve HTTP request  
And so we can proxy requests to application servers  
I want to install and configure a web server

作為一個網站營運工程師 
為了達到，我們可以服務HTTP的請求 
以及，我們可以proxy請求到應用伺服器 
我想安裝和配置Web伺服器 

 
*資料庫 Databases*  
As a web operations engineer working on the service  
So that data can be stored in a manner befitting its structure  
And so the stored data can be queried as quickly as required  
I want to install and configure a suitable database server

作為一個網站營運工程師 
為了達到，使數據能夠被存儲在一個適合它結構的方式 
以及，所存儲存的數據可被快速地根據需要所查詢 
我想安裝和配置一個合適的資料庫伺服器 

As a web operations engineer working on the service  
So that data can still be read even during a failure of a single database server  
I want to configure some failover or other redundancy mechanism for the database

作為一個網站營運工程師 
為了達到，數據在單一資料庫伺服器發生故障時仍然可以被讀取 
我想配置數據庫中的一些故障或其他備援機制 

As a web operations engineer working on the service  
So that data can still be written even during a failure of a single database server  
I want to configure some failover or other redundancy mechanism for the database

作為一個網站營運工程師 
為了達到，數據在單一資料庫伺服器發生故障時仍然可以被寫入儲存
我想配置數據庫中的一些故障或其他備援機制 

*負載均衡 Load balancers*  
As a web operations engineer working on the service  
So that web requests can still be served even with the failure of one or more web servers  
I want to install and/or configure a load balancer
 
作為一個網站營運工程師 
為了達到，使Web請求在單一或多個web伺服器損壞時仍然可以被執行 
我想安裝和/或配置負載平衡器 

*內部DNS Internal DNS*  
As a web operations engineer working on the service  
So that we can easily address our services and instances  
I want to install and/or configure a mechanism to manage internal DNS

作為一個網站營運工程師 
為了達到，我們就可以很容易地解決我們的服務和實例 
我想安裝和/或配置機制來管理內部DNS 

＝＝＝＝＝＝ Sharon 20141111 ＝＝＝＝＝＝＝＝＝＝＝＝
*Database backups*  
As the service manager for the service  
So that we can recover from a large failure of our database infrastructure  
I want regular automated backups to be taken of the data stored in the database

As the service manager for the service  
So that we can recover from a large failure of a single suppliers infrastructure  
I want regular automated backups to be stored off site

數據庫備份 
作為服務管理器的服務 
這樣我們就可以從我們的數據庫基礎設施的大失敗中恢復 
欲要採取存儲在數據庫中的數據的定期自動備份 

作為服務管理器的服務 
這樣我們就可以從一個單一的供應商基礎設施的大失敗中恢復 
我想定期自動備份到存儲場外 

*HTTP cache*  
As a web operations engineer working on the service  
So that the service remains fast when serving identical content  
And so load is minimised on the application servers  
I want to install an HTTP cache

HTTP緩存 
作為一個網絡運營工程師，從事服務 
從而使服務保持快速服務相同的內容時， 
等載荷最小化的應用程序服務器上 
我想安裝一個HTTP緩存 

*Email gateway*  
As a developer working on the service  
So that the service can send email to administrators or end users  
I want to setup and configure a suitable email gateway

電子郵件網關 
作為一名開發人員工作的服務 
因此，該服務可以發送電子郵件給管理員或最終使用者 
我想設置和配置適當的電子郵件網關 

*Application servers*  
As a developer working on the service  
So that the code I write can be run on server instances  
I want to install and configure a suitable application server

應用服務器 
作為一名開發人員工作的服務 
所以，我寫的代碼可以在服務器實例上運行 
我想安裝和配置一個合適的應用服務器 

*Internal package repository*  
As a web operations engineer working on the service  
So that we can use software not available in our operating system repositories  
And so that we can use the security, dependency management and versioning features  
I want to install and configure an internal package repository

內部包庫 
作為一個網絡運營工程師，從事服務 
這樣我們就可以使用不可用的軟體在我們的操作系統庫 
因此，我們可以使用的安全性，依賴管理和版本控制功能 
我想安裝和配置內部包庫 

*Artifact repository*  
As a developer working on the service  
So that we can share and version individual code components that need it  
I want to install and configure an artifact repository

神器資料庫 
作為一名開發人員工作的服務 
這樣我們就可以共享和版本單獨代碼組件需要它 
我想安裝和配置工件儲存庫 

*Message queue*  
As a developer working on the service  
So that I can easily and efficiently process work asynchronously  
I want to install and configure a suitable message queue or work queue system

消息隊列 
作為一名開發人員工作的服務 
這樣我就可以方便，高效地處理異步工作 
我想安裝和配置合適的消息隊列或工作隊列系統 

*Search server*  
As a developer working on the service  
So that I can quickly and efficiently search through large amounts of data  
I want to install and configure a suitable search engine

搜索服務器 
作為一名開發人員工作的服務 
這樣我就可以通過大量的數據快速，高效地搜索 
我想安裝和配置一個合適的搜索引擎 

*Object cache*  
As a developer working on the service  
So that I can minimise the number of queries to the database  
And so that I can keep the service fast and responsive to users  
I want to install and configure a object caching system

對象緩存 
作為一名開發人員工作的服務 
這樣我就可以查詢的數量最小化到數據庫 
而且，這樣我可以保持服務快速響應使用者 
我想安裝和配置對象緩存系統

### Monitoring 監控

*Metric collection service*  
As a web operations engineer working on the service  
So that we can collect large numbers of time series metrics from the running service  
I want to install and configure a metric collection system

指標收集服務 
作為一個網絡運營工程師，從事服務 
這樣我們就可以收集大量的時間序列指標從正在運行的服務 
我想安裝和配置指標收集系統 

*Application running monitoring checks*  
As a web operations engineer working on the service  
So that we can run checks against metrics from the metrics system  
And so that we can run active checks based on arbitrary code  
I want to install and configure a monitoring system

運行的應用程序的監控檢查 
作為一個網絡運營工程師，從事服務 
這樣我們就可以對運行在指標體系的指標檢查 
基於任意代碼，並讓我們可以運行檢查活動 
我想安裝和配置監測系統 

*Smoke tests*  
As a developer working on the service  
So that I know that I haven’t broken anything when deploying my application  
I want a series of smoke tests to be run after all deployments

煙霧測試 
作為一名開發人員工作的服務 
所以，我知道，我沒有破壞任何東西我在部署應用程序時， 
我想所有的部署後運行一系列的煙霧測試 

*Application metrics*  
As a developer working on the service  
So that I can gain visibility of how my application is running in production  
And so we can find and fix problems with it quickly  
I want a simple way of instrumenting my application to feed metrics to the metrics system

申請指標 
作為一名開發人員工作的服務 
這樣我就可以得到我如何應用在生產環境中運行的可見性 
因此，我們可以發現並迅速解決問題，這 
我想插裝我的應用程序的一個簡單的方法來養活度量的指標體系 

*System metrics*  
As a web operations engineer working on the service  
So that we can identify and fix problems with the system, ideally before they occur  
I want to set up collection of low level system metrics like load, disk, network io, etc.

系統指標 
作為一個網絡運營工程師，從事服務 
這樣我們就可以發現並解決系統問題，出現理想才 
我想成立集合類負載，磁盤，網絡IO等低級別的系統指標 

*Security monitoring*  
As a web operations engineer working on the service  
So that we notice quickly and are alerted to any incidents with a security flavour  
I want to configure suitable security monitoring tools

安防監控 
作為一個網絡運營工程師，從事服務 
所以，我們看到快速被驚動任何事故與安全性味 
我想配置合適的安全監控工具 

*Notifications*  
As a web operations engineer or developer supporting the service  
So that I know about any issues as they happen  
I want to set up suitable notifications from the monitoring system

通知 
作為一個網絡運營工程師或開發人員支持服務 
所以，我知道的任何問題，因為它們發生 
我要建立適當的通知，從監控系統 

*Transactional monitoring*  
As a developer working on a transactional service  
So that we can block fraudulent or otherwise suspect transactions  
I want to install and configure a transactional monitoring system with suitable rules

事務監察 
作為一名開發人員工作的一個事務服務 
這樣我們就可以阻止欺詐或其他犯罪嫌疑人交易 
我想安裝並配置事務監控系統適用規則 

*External monitoring*
As the service manager for the service  
So that in the event of a failure of the monitoring system  
And so that the service is monitoring from outside our local network  
I want an external monitoring capability with basic checks to monitoring service uptime

外部監督作為服務經理服務 
所以，在監視系統的故障的情況下 
因此，該服務是從本地網絡以外的監督 
我想基本的檢查，以監測服務正常運行時間的外部監控能力 

*Monitoring data feed from infrastructure provider*  
As a web operations engineer working on the service  
So that I am aware of problems in the hypervisor, physical or network infrastructure  
I want a feed of monitoring data from the Infrastructure supplier

從基礎設施提供商的監測數據進 
作為一個網絡運營工程師，從事服務 
讓我知道，在虛擬機管理程序的問題，身體或網絡基礎設施 
我想從基礎設施供應商的原料監測數據 

### Logging 日誌 

*Log collection*  
As a web operations engineer working on the service  
So that I can easily see everything that is happening in specific applications  
I want to collect all the logs from applications running on the same host in one place

日誌收集 
作為一個網絡運營工程師，從事服務 
所以，我可以很容易地看到的一切，是發生在特定的應用程序 
我想收集所有日誌來自同一主機上的在同一個地方運行的應用程序 

*Log aggregation*  
As a web operations engineer working on the service  
So that I don't have to go to an individual machine to view its logs  
I want all logs from all machines to be aggregated together

日誌聚合 
作為一個網絡運營工程師，從事服務 
所以，我不用去個別的機器，查看其日誌 
我想所有計算機的所有日誌聚合在一起 

*Log storage*
As a web operations engineer working on the service  
So that logs can be kept for a suitable period of time  
I want to provision enough storage for log archiving

日誌存儲
作為一個網絡運營工程師，從事服務 
從而能夠保持適當的時間週期記錄 
我要提供足夠的存儲空間日誌歸檔 

*Log viewing*
As a web operations engineer working on the service  
So that I can see what is happening across the infrastructure  
I want a mechanism for viewing and searching logs in as near real time as possible

As a developer working on the service  
So that I can extract information from logs to aid with improving the service  
I want a mechanism to run queries across the aggregated logs

查看日誌
作為一個網絡運營工程師，從事服務 
這樣我就可以看到正在發生的事情在整個基礎架構 
我希望有一個機制，用於查看和搜索日誌中的近實時地 

作為一名開發人員工作的服務 
這樣我就可以提取日誌信息，以幫助與改善服務 
我想運行在整個聚合日誌查詢機制 

### Configuration management 配置管理

*Configuration management client*  
As a web operations engineer working on the service  
So that changes to server configuration can be made safely and quickly  
I want to install software to manage configuration management

配置管理客戶端 
作為一個網絡運營工程師，從事服務 
以便改變服務器的配置能夠安全且迅速地進行 
我想安裝軟體來管理配置管理 

*Configuration management database*
As a web operations engineer working on the service  
So that configuration changes are tracked over time  
And so that current state of available to query  
I want to install software to manage a configuration management database

配置管理數據庫
作為網絡運營工程師，從事服務 
使配置更改跟踪一段時間 
因此可用的，當前的狀態進行查詢 
我想安裝軟體來管理配置管理數據庫 

*Configuration management server*  
As a web operations engineer working on the service  
So that all nodes do not have all configuration information  
I want to install software to allow centralised management of Configuration management code

配置管理服務器 
作為一個網絡運營工程師，從事服務 
這樣所有節點不具有所有的配置信息 
我想安裝的軟體，允許配置管理代碼的集中管理 

### Deployment 部署 

*Configuration management code deployment mechanism*  
As a web operations engineer working on the service  
So that configuration changes can be made safely and in an auditable manner  
I want a deployment process and tooling for configuration management code

配置管理代碼部署機制 
作為一個網絡運營工程師，從事服務 
使配置更改可以安全地和可審計的方式進行 
我希望有一個部署流程和工具用於配置管理的代碼 

*Application deployment mechanism*  
As a developer working on the service  
So that changes to applications can be made available to users  
And so that changes are made in a safe and auditable manner  
I want a deployment process and tooling for application code

應用部署機制 
作為一名開發人員工作的服務 
使更改應用程序可以提供給使用者 
而這樣的變化在一個安全和可審計的方式取得 
我希望有一個部署流程和工具的應用程序代碼 

*Release tracking*  
As the service manager for the service  
So that we have an auditable log of what was changed when by whom  
I want an up-to-date list of releases to be maintained

發行追踪 
作為服務管理器的服務 
所以，我們有什麼改變由誰來當審計的日誌 
我想保持到發布的高達最新名單 

*Packaging*  
As a web operations engineer working on the service  
So that we don’t have to compile customised applications from source before using them  
And so we can take advantage of dependency and version management capabilities of the OS  
I want a process and tooling for creating our own system packages

包裝 
作為一個網絡運營工程師，從事服務 
所以，我們並沒有使用它們之前，從源碼編譯自定義應用程序 
因此，我們可以利用操作系統的依賴和版本管理功能的優勢 
我要創造我們自己的系統封裝工藝和工裝 

*Orchestration*  
As a web operations engineer working on the service  
So that I can run commands across multiple instances quickly  
I want tooling in place which allows some orchestration based on the current instances

業務流程 
作為一個網絡運營工程師，從事服務 
這樣我就可以快速運行多個實例的命令 
欲代替模具，它允許某些業務流程基於當前實例 

*Database migrations*  
As a web operations engineer working on the service  
So that I can have confidence that database migration scripts will work when applied to production  
I want database migrations to be deployed through the same sequence of environments as code changes  

數據庫遷移 
作為一個網絡運營工程師，從事服務 
這樣我可以有信心，當應用到生產數據庫遷移腳本將工作 
我想數據庫遷移，通過環境的代碼更改的相同順序進行部署 

*Management of secrets*  
As a web operations engineer working on the service  
So that I can ensure confidential communication between particular parts of the system  
I want a process or tool for managing secrets such as keys and passwords

秘密管理 
作為一個網絡運營工程師，從事服務 
所以，我可以保證系統的特定部分之間的保密通信 
我希望有一個管理的秘密，如密鑰和密碼的過程或工具 

### Access control 訪問控制

*End user devices*  
As the service manager responsible for the service  
So that management access to the infrastructure can be locked down to prevent unauthorised access  
I want to know what kind of protection the management end user devices require

終端使用者設備 
作為服務經理，負責服務 
因此，在基礎設施，管理訪問可以被鎖定，以防止未經授權的訪問 
我想知道什麼樣的保護管理最終使用者設備要求 

*User directory*  
As a web operations engineer  
So that we do not have to maintain multiple lists of privileged users  
And so that users can be added and removed once in a central fashion  
I want to install and configure something to provide a single user directory

使用者目錄 
作為一個網絡運營工程師 
這樣我們就不必維護特權使用者的多個列表 
並且，這樣使用者就可以增加，並在中央的方式除去一次 
我想安裝和配置的東西，以提供一個單一的使用者目錄 

*Key based authentication*  
As a web operations engineer  
So that we are not vulnerable to password based login attempts to individual servers  
I want to set-up public key based authentication

基於密鑰認證 
作為一個網絡運營工程師 
所以，我們不容易受到基於密碼的登錄嘗試，以單台服務器 
我要建立基於公共密鑰的認證 

*Single sign-on*  
As a web operations engineer  
So that any third party web interfaces we use can be accessed via a single login  
I want to install and configure a single sign-on systems

單點登錄 
作為一個網絡運營工程師 
因此，我們使用任何第三方的Web界面可以通過一個單一的登錄訪問 
我想安裝和配置單點登錄系統 

*Network/VPN configuration*  
As a web operations engineer  
So that management functions can not be accessed via the public internet  
And so that we reduce the surface area for attack  
I want to restrict management access to a VPN and/or non-public restricted network

網絡/ VPN配置 
作為一個網絡運營工程師 
使管理職能無法通過公共互聯網訪問 
並且使我們減少了表面積為攻 
我想限制到VPN和/或非公開的受限網絡訪問管理 

### Provisioning 供應

*Other environments*  
As the service manage for the service  
So that I can see the very latest working version of the service at any time  
And so I can share that with people in and outside the team  
I want a preview environment to be provisioned which is similar to production

As a web operations engineer working on the service  
So that the we have a clean environment in which to test production deployments  
And so that we have a secure environment to test with production-like data  
I want to provision a staging environment which mimics production as closely as possible

其他環境 
作為服務管理的服務 
這樣我就可以看到服務的最新版本工作在任何時候 
所以，我可以分享的人在和球隊之外 
我希望有一個預覽環境中置備這是類似生產 

作為一個網絡運營工程師，從事服務 
從而使我們有一個乾淨的環境中進行測試的生產部署 
因此，我們有一個安全的環境中測試與生產類數據 
我想提供一個臨時的環境，為密切模仿生產地 

*Production environment*  
As a web operations engineer working on the service  
So that the service can launch to the public  
I want to provision a production environment

生產環境 
作為一個網絡運營工程師，從事服務 
因此，該服務可以啟動公眾 
我想提供生產環境 

*Base image(s)*  
As a web operations engineer working on the service  
So that all server instances start out with sensible security settings  
I want to create a base image running the chosen operating system with hardened configuration

基本圖像（S） 
作為一個網絡運營工程師，從事服務 
使所有服務器實例開始與合理的安全設置 
我想創建運行所選擇的操作系統硬化配置的基本圖像 

*Public network interfaces*  
As a web operations engineer working on the service  
So that the application only receives wanted traffic from the internet  
And so that we don’t accidentally expose sensitive or insecure components of the system  
I want to configure and test the public network interfaces for the system

公共網絡接口 
作為一個網絡運營工程師，從事服務 
使應用程序只接收想要的流量來自互聯網 
因此，我們不小心露出的系統的敏感或不安全的部件 
我想配置和測試公共網絡接口的系統 

*Private network configuration*  
As a web operations engineer working on the service  
So that individual internal components can only talk with known parts of the system  
And so we limit the extent of any security breach  
I want to configure and test the private network interfaces for the system

私人網絡配置 
作為一個網絡運營工程師，從事服務 
使單獨的內部組件可以只使用系統的公知的部件說話 
所以我們限制的安全漏洞的程度 
我想配置和測試專用網絡接口，為系統 

*Network codes of connection*  
As a web operations engineer working on the service  
Given I need to communicate with a system only available on a Government network  
So that the two systems can talk with each other  
I want to meet the code of connection requirements and configure access to the network

連接網絡代碼 
作為一個網絡運營工程師，從事服務 
由於我需要一個系統的通信只提供政府網 
因此，這兩個系統可以與對方通話 
我想，以滿足連接條件的代碼，並配置到網絡接入 

*Management network*  
As a web operations engineer working on the service  
So that network traffic used to manage the infrastructure is separate from public traffic  
And so we can monitor irregularities in network traffic separately  
I want to configure a separate management network

管理網絡 
作為一個網絡運營工程師，從事服務 
因此，用於管理基礎設施的網絡流量是分開的公共交通 
因此，我們可以單獨監控網絡流量違規 
我想配置一個單獨的管理網絡 

*Platform load balancers*  
As a web operations engineer working on the service  
So that we can reduce the number of single points of failure  
And so that we can scale out to deal with a large amount of traffic  
I want to provision load balancers to distribute traffic between multiple instances

平台的負載均衡 
作為一個網絡運營工程師，從事服務 
這樣我們就可以減少單點故障的數量 
因此，我們可以擴展到處理大量的流量 
我要提供負載均衡分配多個實例之間的通信 

*Platform firewalls*  
As a web operations engineer working on the service  
So that unwanted traffic can be filtered before it enters our virtual infrastructure  
I want to configure the external facing IaaS firewalls to only allow certain traffic

平台的防火牆 
作為一個網絡運營工程師，從事服務 
所以，它進入我們的虛擬基礎架構之前不需要的流量進行過濾 
我想配置外部面臨的IaaS防火牆，只允許特定的流量 

*Dynamic environments*  
As a web operations engineer working on the service  
So that we are not constrained by a fixed number of environments  
And so we can easy run full stack tests or experiments  
I want to be able to easily provision an environment running the full service

動態環境 
作為一個網絡運營工程師，從事服務 
所以，我們不是由環境中固定數目的限制 
因此，我們可以輕鬆運行完整的協議棧的測試或實驗 
我想能夠輕鬆運行提供全方位服務的環境 

*Elastic scaling*  
As a web operations engineer working on the service  
So that the service can automatically deal with unexpected increases in traffic  
I want to configure tooling to automatically scale the number of instances based on load

彈性縮放 
作為一個網絡運營工程師，從事服務 
因此，該服務可以自動應對突發流量增長 
欲配置工具來自動縮放的實例的數量根據負荷 

### Security controls 安全控制 

*Operating system hardening*  
As a web operations engineer  
So that we are making use of built-in operating system security controls  
I want to automate a default set of hardening rules for our chosen operating system

操作系統硬化 
作為一個網絡運營工程師 
因此，我們利用內置的操作系統的安全控制 
我想自動硬化規則的默認設置為我們所選擇的操作系統 


*Malware detection*  
As a web operations engineer  
So that instances which may be compromised can be dealt with quickly  
I want to automate the detection of potential malware

惡意軟體檢測 
作為一個網絡運營工程師 
使得其可以被破壞，可迅速處理的實例 
我想自動潛在惡意軟體的檢測 

*Intrusion detection*  
As a web operations engineer  
So that instances which are being attacked or probed can defend themselves  
I want to configure an intrusion detection and prevention system

入侵檢測 
作為一個網絡運營工程師 
這樣，所受到攻擊或探測實例可以為自己辯護 
我想配置入侵檢測和預防系統 

*Virus scanning*  
As a web operations engineer  
So we can be sure that files in the system don't have viruses  
I want to install virus scanning for files passing a network boundary

病毒掃描 
作為一個網絡運營工程師 
因此，我們可以肯定的是，在系統文件沒有病毒 
我想安裝病毒掃描的文件通過網絡邊界 

*Host firewalls*  
As a web operations engineer  
So that the surface area for attack is limited  
And so that services which should only be available locally aren't exposed on the internet  
I want to install and configure a local firewall

主機防火牆 
作為一個網絡運營工程師 
使得表面積為攻擊被限制 
因此，這應該只能在本地提供的服務不被暴露在互聯網上 
我想安裝和配置本地防火牆 

*On instance event auditing*  
As a web operations engineer  
So that I know when things like logins or other sensitive events happen on instances  
I want to set-up some auditing of events

在實例事件審計 
作為一個網絡運營工程師 
所以，我知道當事情像登錄或其他敏感事件發生的情況下， 
我要建立事件的一些審計 

*Rate/connection limiting*  
As a web operations engineer  
So that large spikes in traffic from a single source don't overwhelm application  
I want to configure some level of rate and connection limiting for web requests

速度/連接限制 
作為一個網絡運營工程師 
從單一來源，這樣大的流量高峰沒有壓倒的應用 
我想配置的速度和連接一定程度上限制了Web請求 

*Secure storage of key material*  
As a web operations engineer  
So that any highly sensitive cryptographic keys are not lost, resulting in a compromise  
I want to have a mechanism in place to securely store key material

對關鍵材料的安全存儲 
作為一個網絡運營工程師 
因此，任何高度敏感的加密密鑰不被丟失，從而導致一種折衷 
我想有地方安全地存儲密鑰材料的機制 

*Third party DDoS protection*  
As a web operations engineer  
So that a the site does not go down under a denial of service attack  
I want to purchase and/or configure a level of DDoS protection

第三方的DDoS防護 
作為一個網絡運營工程師 
所以，一個網站沒有根據的拒絕服務攻擊下去 
我想購買和/或配置的DDoS保護級別 

### Testing 測試 

*Performance testing*  
As the service manager responsible for the service  
So that we know the service will be fast and responsive under realistic traffic  
I want to be able to run a comprehensive performance test suite against the service

性能測試 
作為服務經理，負責服務 
這樣我們就知道該服務將快速反應在真實的交通 
我想能夠對服務運行綜合性能測試套件 

*As a developer working on the service*  
So that we know changes to the code do not negatively affect performance  
I want the performance test suite to run as part of the continuous integration system

作為一名開發人員工作的服務 
這樣我們就知道修改代碼不性能產生負面影響 
我想要的性能測試套件，以作為持續集成系統的一部分運行 

*Load testing*  
As the service manager responsible for the service  
So that we know the service will still be working under larger amounts of traffic than are expected  
I want to be able to run a comprehensive load test suite against the service

負載測試 
作為服務經理，負責服務 
這樣我們就知道該服務仍將受到較大的交通量工作比預期 
我想能夠對服務運行的全面負載測試套件 

*Application penetration testing*  
As the service manager responsible for the service  
So that the service does not get compromised due to a vulnerability  
And so we meet our accreditation obligations  
I want to run a suitable number of penetration tests against the applications under development

應用程序滲透測試 
作為服務經理，負責服務 
因此，該服務不會得到應有的妥協，以漏洞 
因此，我們滿足我們的認可義務 
我想運行對正在開發的應用程序的適當數目的滲透測試 

*As the service manager responsible for the service*  
So that the service does not get compromised due to a vulnerability  
And so we meet our accreditation obligations  
I want to run a suitable number of penetration tests against third party installed applications used as part of the service

作為服務經理，負責服務 
因此，該服務不會得到應有的妥協，以漏洞 
因此，我們滿足我們的認可義務 
我想對運行作為服務的一部分，第三個安裝第三方應用適當數量的滲透測試 

*Infrastructure penetration testing*  
As the service manager responsible for the service  
So that the service does not get compromised due to a vulnerability  
And so we meet our accreditation obligations  
I want to run a suitable number of penetration tests against the infrastructure configuration

基礎設施的滲透測試 
作為服務經理，負責服務 
因此，該服務不會得到應有的妥協，以漏洞 
因此，我們滿足我們的認可義務 
我要對基礎設施的配置中運行的滲透測試一個合適的數量 

### Operating system 操作系統

*Operation system selection*  
As a web operations engineer working on the service  
So that we have a clear path to receiving security updates  
And so we can more easily find support for our systems  
I want to select and install a suitable default operating system for the service

操作系統的選擇 
作為一個網絡運營工程師，從事服務 
因此，我們有一個清晰的路徑來接收安全更新 
因此，我們可以更容易找到我們的系統支持 
我想選擇和安裝合適的默認操作系統服務 

*File systems*  
As a web operations engineer working on the service  
So that we get the best possible performance and reliability from the disk  
I want to select a suitable file system and partition layout

文件系統 
作為一個網絡運營工程師，從事服務 
讓我們從盤面最佳的性能和可靠性 
我要選擇一個合適的文件系統和分區佈局 

*Resource isolation*  
As a web operations engineer working on the service  
So that noisy applications cannot affect other applications on the instance  
I want to be able to isolate running applications from each other in terms of memory and CPU

資源隔離 
作為一個網絡運營工程師，從事服務 
讓嘈雜的應用程序不能影響到該實例的其他應用程序 
我想能夠分離出的內存和CPU上運行的相互應用 

*Read-only file systems*  
As a web operations engineer working on the service  
So that I can protect against files being changed due to compromises in the application  
I want to be able to configure a read-only file system if appropriate.

只讀文件系統 
作為一個網絡運營工程師，從事服務 
這樣我就可以防止文件被因在申請變更為妥協 
我想能夠在適當配置只讀文件系統。
