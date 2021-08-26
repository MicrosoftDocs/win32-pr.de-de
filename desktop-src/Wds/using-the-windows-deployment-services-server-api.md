---
title: Verwenden der Server-API der Windows-Bereitstellungsdienste
description: In Umgebungen, in denen die Standardlösung Windows Deployment Services (WDS) nicht verwendet werden kann, macht der WDS-Server eine API verfügbar, mit der Entwickler Plug-Ins schreiben können, die als Anbieter bezeichnet werden, um PXE-Anforderungen (Preboot Execution Environment) zu verarbeiten.
ms.assetid: 5e25654a-33c6-4c0f-acc3-e938d1f4a4e7
keywords:
- Windows Bereitstellungsdienste Windows Bereitstellungsdienste mithilfe der Server-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ce7516e5279fecdfeecfa90edd8e3a0dad265562fa5ea59336367dbe157c5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999570"
---
# <a name="using-the-windows-deployment-services-server-api"></a>Verwenden der Server-API der Windows-Bereitstellungsdienste

In Umgebungen, in denen die Standardlösung Windows Deployment Services (WDS) nicht verwendet werden kann, macht der WDS-Server eine API verfügbar, mit der Entwickler Plug-Ins schreiben können, die als Anbieter bezeichnet werden, um PXE-Anforderungen (Preboot Execution Environment) zu verarbeiten. Entwickler sollten beim Schreiben von PXE-Anbietern für WDS die folgenden Richtlinien einhalten.

## <a name="install-the-wds-role-on-the-server"></a>Installieren der WDS-Rolle auf dem Server

-   Windows Bereitstellungsdienste (Deployment Services, WDS) ist die überarbeitete Version der Remoteinstallationsdienste (REMOTE Installation Services, RIS). Sie benötigen die WDS-Serverrolle, um den WDS-PXE-Server und -Anbieter zu implementieren.
-   WDS ersetzt RIS als Standardkomponente ab Windows Server 2008 und Windows Server 2003 durch Service Pack 2 (SP2).
-   Sie müssen den RIS-Server mit Service Pack 1 (SP1) auf Windows Server 2003 auf WDS aktualisieren. Sie können die WDS-Serverrolle mit dem [Windows Automated Installation Kit (CSVK)](https://www.microsoft.com/download/details.aspx?id=10333)installieren.

## <a name="register-providers"></a>Registrieren von Anbietern

-   Registrieren Sie die Dynamic Link Library (DLL) des Anbieters während der Installation, und fügen Sie den Anbieter in die geordnete Liste der registrierten Anbieter ein.
    > [!Note]  
    > Wenn Sie einen neuen oder geänderten Anbieter installieren, müssen Sie den WDS-PXE-Dienst neu starten, damit die Änderungen wirksam werden.

     

-   Verwenden Sie die [**PxeProviderRegister-Funktion,**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister) um den Anbieter zu registrieren und der Liste hinzuzufügen. Verwenden Sie die [**PxeProviderUnRegister-Funktion,**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderunregister) um die Registrierung eines registrierten Anbieters aufzuheben und ihn aus der Liste zu entfernen.
-   Geben Sie die Reihenfolge des Anbieters in der sortierten Liste an. Der Index eines Anbieters in der Liste kann nicht garantiert werden, da später möglicherweise ein anderer Anbieter registriert wird. Um den Anbieter vor oder nach einem anderen registrierten Anbieter in die Liste einzufügen, verwenden Sie zunächst die [**PxeProviderQueryIndex-Funktion,**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex) um den Index des registrierten Anbieters abzurufen, und registrieren Sie dann den neuen Anbieter, während Sie einen größeren oder kleineren Indexwert angeben.
-   Die Installation kann Anbieterkonfigurationsinformationen unter dem Registrierungsschlüssel speichern, der beim Registrieren des Anbieters zurückgegeben wird. Die Adresse des Registrierungsschlüssels wird vom *phProviderKey* von [**PxeProviderRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister)empfangen. Der Anbieter empfängt ein Handle für denselben Schlüssel wie der *hProviderKey-Parameter* für seinen [*PxeProviderInitialize-Rückruf.*](pxeproviderinitialize.md) Der Anbieter sollte die Adresse dieses Schlüssels speichern.
-   Installieren Sie immer die Dynamic Link Library (DLL) des Anbieters im Ordner Programme des Servers.

## <a name="initialize"></a>Initialisieren

-   Schließen Sie eine DLL ein, die die [*Rückruffunktion PxeProviderInitialize*](pxeproviderinitialize.md) im Anbieter exportiert. Jeder Anbieter erfordert einen *PxeProviderInitialize-Rückruf.* Wenn WDS einen Anbieter lädt, ruft es die *PxeProviderInitialize-Funktion* des Anbieters auf und übergibt ein Handle an denselben Schlüssel, der zum Speichern von Konfigurationsinformationen während der Anbieterregistrierung verwendet wird.
-   Wenn der [*PxeProviderInitialize-Rückruf*](pxeproviderinitialize.md) zurückgegeben wird und erfolgreich ist, sollte der Anbieter vollständig initialisiert und für die Verarbeitung von Anforderungen bereit sein.
-   Registrieren Sie jeden Rückruf im Anbieter während der Verarbeitung der [*PxeProviderInitialize-Funktion.*](pxeproviderinitialize.md) Rückrufe sollten bei der [**PxeRegisterCallback-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) registriert werden.
-   Initialisieren Sie alle internen Ressourcen des Anbieters innerhalb der Verarbeitung seiner [*PxeProviderInitialize-Funktion.*](pxeproviderinitialize.md)

## <a name="shutdown"></a>Herunterfahren

-   Implementieren Sie den [*PxeProviderShutdown-Rückruf.*](pxeprovidershutdown.md) Jeder Anbieter muss über einen *PxeProviderShutdown-Rückruf* verfügen.
-   Die [*Rückruffunktion PxeProviderShutdown*](pxeprovidershutdown.md) sollte den Anbieter vollständig herunterfahren und alle zugehörigen Ressourcen freigeben.
-   Nachdem der [*PxeProviderShutdown-Rückruf*](pxeprovidershutdown.md) zurückgegeben wurde, ist das an die [*PxeProviderInitialize-Funktion übergebene*](pxeproviderinitialize.md) *hProvider-Handle* nicht mehr gültig und sollte nicht zum Aufrufen von WDS verwendet werden.
-   Registrieren Sie den [*PxeProviderShutdown-Rückruf,*](pxeprovidershutdown.md) indem Sie während der Verarbeitung des [*PxeProviderInitialize-Rückrufs*](pxeproviderinitialize.md) die [**PxeRegisterCallback-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) mit **PXE \_ CALLBACK \_ SHUTDOWN** aufrufen. Rufen Sie den *PxeProviderShutdown-Rückruf* nicht auf, wenn die *PxeProviderInitialize-Funktion* fehlschlägt.

## <a name="handle-request-packet"></a>Verarbeiten des Anforderungspakets

Implementieren Sie den [*PxeProviderRecvRequest-Rückruf*](pxeproviderrecvrequest.md) für den Anbieter. Jeder Anbieter muss über einen *PxeProviderRecvRequest-Rückruf* verfügen. Wenn WDS eine Anforderung empfängt, ruft es den *PxeProviderRecvRequest-Rückruf* für den ersten Anbieter in der Liste der registrierten Anbieter auf.

-   Wenn der Anbieter diese Anforderung synchron verarbeitet, sollte die [*PxeProviderRecvRequest-Funktion*](pxeproviderrecvrequest.md) den Wert **ERROR \_ SUCCESS** zurückgeben. Wenn und nur dann, wenn der Anbieter diese Anforderung asynchron verarbeitet, sollte der *PxeProviderRecvRequest-Rückruf* **ERROR IO \_ \_ PENDING** zurückgeben und die [**PxeAsyncRecvDone-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) aufrufen, wenn die Anforderung verarbeitet wurde.
-   Der [*PxeProviderRecvRequest-Rückruf*](pxeproviderrecvrequest.md) und die [**PxeAsyncRecvDone-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) geben die Adresse einer **PXE \_ BOOT \_ ACTION-Enumeration** zurück, die die Aktion beschreibt, die vom Anbieter zur Verarbeitung der Anforderung ausgeführt wird.

    Es gibt vier Möglichkeiten für einen Anbieter, eine Anforderung zu verarbeiten:

    -   Der Anbieter antwortet dem Client mit einem DHCP-Standardantwortpaket, das einen Pfad zum Netzwerkstartprogramm enthält. Das Zurückgeben des **PXE \_ BA \_ NBP-Werts** für die Enumeration bedeutet, dass der Anbieter das Anforderungspaket erfolgreich verarbeitet und die Anforderung durch Senden eines Antwortpakets durch Aufrufen der Funktionen [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) und [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) abgeschlossen hat.
    -   Der Anbieter antwortet dem Client mit einem benutzerdefinierten Antwortpaket, das dhcp nicht entspricht. Das Zurückgeben des **PXE \_ BA \_ CUSTOM-Werts** für die Enumeration bedeutet, dass der Anbieter das Anforderungspaket erfolgreich verarbeitet und die Anforderung durch Senden eines benutzerdefinierten Antwortpakets durch Aufrufen der Funktionen [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) und [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) abgeschlossen hat.
    -   Der Anbieter bestimmt, dass die Anforderung ignoriert werden soll. Das Zurückgeben des **PXE \_ BA \_ IGNORE-Werts** für die Enumeration bedeutet, dass der Anbieter alle Ressourcen freigegeben hat, die der Anforderung zugeordnet sind, und die Anforderung wird nicht an den nächsten Anbieter in der Liste der registrierten Anbieter übergeben. Anbieter können diese Option verwenden, wenn sie feststellen, dass ein Anforderungspaket ungültig ist.
    -   Der Anbieter lehnt es ab, die Anforderung zu bedienen. Die Rückgabe des **PXE \_ BA \_ REJECT-Werts** für die Enumeration weist das System an, die Anforderung an den nächsten Anbieter in der Liste der registrierten Anbieter zu übergeben. Wenn dies der letzte Anbieter in der Liste war, werden alle ressourcen, die der Anforderung zugeordnet sind, veröffentlicht, und die Anforderung wird ignoriert.
    -   Registrieren Sie den [*PxeProviderRecvRequest-Rückruf,*](pxeproviderrecvrequest.md) indem Sie während der Verarbeitung des [*PxeProviderInitialize-Rückrufs*](pxeproviderinitialize.md) die [**PxeRegisterCallback-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) mit **PXE \_ CALLBACK \_ RECV \_ REQUEST** aufrufen.

## <a name="generate-response-packet"></a>Generieren eines Antwortpakets

-   Verwenden Sie die API, um Anbieter zu schreiben, um DHCP-Anforderungen zu verarbeiten und Antwortpakete zu generieren.
-   Die [**PxeProviderSetAttribute-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) gibt die Attribute an, die vom Anbieter zum Filtern von Paketen verwendet werden. Die Attribute des Anbieters können so angegeben werden, dass der Anbieter alle Pakete sieht, der Anbieter nur DHCP-Pakete oder nur DHCP-Pakete sieht, die die DHCP-Anbieterklassen-ID (60) als "PXEClient" angeben.
-   Die [**PxeDhcpIsValid-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpisvalid) überprüft, ob ein Paket ein gültiges DHCP-Paket ist. Anbieter können die **PxeDhcpIsValid-Funktion** verwenden, um zu überprüfen, ob ein Paket vom Client ein DHCP-Paket ist, wenn der Filtersatz mit der [**PxeProviderSetAttribute-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) so festgelegt ist, dass alle Pakete empfangen werden, um zu bestimmen, ob ein angegebenes Paket ein gültiges DHCP-Paket ist.
-   Die [**PxeDhcpInitialize-Funktion initialisiert**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpinitialize) ein Antwortpaket als DHCP-Antwortpaket, das auf den Informationen in einem vom Client empfangenen Paket basiert. Die [*PxeProviderInitialize-Funktion*](pxeproviderinitialize.md) übernimmt die Adresse eines gültigen DHCP-Pakets, das vom Client im [*PxeProviderRecvRequest-Rückruf*](pxeproviderrecvrequest.md) empfangen wird. Die **PxeDhcpInitialize-Funktion** verwendet einen Zeiger auf ein Antwortpaket, das der [**PxePacketAllocate-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) zugeordnet ist.
-   Die [**PxeDhcpGetOptionValue-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue) ruft einen Optionswert aus einem DHCP-Paket ab. Die [**PxeDhcpGetVendorOptionValue-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) ruft einen Optionswert aus dem Feld Vendor Specific Information (43) eines DHCP-Pakets ab.
-   Der Anbieter kann dann das Antwortpaket mit Informationen auffüllen und die [**PxeSendReply-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) verwenden, um das Antwortpaket an den Client zu senden. Die [**PxeDhcpAppendOption-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpappendoption) fügt eine DHCP-Option an das Antwortpaket an.
-   Ein Anbieter, der auf Clientanforderungen durch Senden eines Pakets antwortet, muss das Antwortpaket mithilfe der [**PxePacketAllocate-Funktion zuordnen.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) Der Anbieter kann dann das Antwortpaket mit Informationen auffüllen und die [**PxeSendReply-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) verwenden, um das Antwortpaket an den Client zu senden.
-   Wenn der zugeordnete Arbeitsspeicher nicht mehr benötigt wird, sollte der Anbieter ihn mithilfe der [**PxePacketFree-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketfree) freigeben.

## <a name="enumerate-registered-providers"></a>Aufzählen registrierter Anbieter

-   Verwenden Sie die API, um Anbieter zu schreiben, die andere registrierte Anbieter in der Liste auflisten und überprüfen.
-   Die [**PxeGetServerInfo-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxegetserverinfo) gibt Informationen zum PXE-Server zurück. Die **PxeGetServerInfo-Funktion** gibt eine **BOOL** zurück, die angibt, ob die Ablaufverfolgung für den Server aktiviert ist. **TRUE** gibt an, dass die Ablaufverfolgung aktiviert ist.
-   Die [**PxeProviderEnumFirst-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst) startet einen enumerationof-Anbieter in der Liste der registrierten Anbieter. Die **PxeProviderEnumFirst-Funktion** startet die -Enumeration und gibt die Adresse des Handles zurück, das beim Aufrufen der [**PxeProviderEnumNext-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumnext) verwendet werden soll. Die **PxeProviderEnumNext-Funktion** gibt eine [**PXE \_ PROVIDER-Struktur**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider) zurück, die die Informationen zum Anbieter enthält. Die [**PxeProviderFreeInfo-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo) gibt den Arbeitsspeicher frei, der von der **PxeProviderEnumNext-Funktion** für die **PXE \_ PROVIDER-Struktur** zugeordnet wurde. Die [**PxeProviderEnumClose-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumclose) schließt die Enumeration von Anbietern in der Liste der registrierten Anbieter.

## <a name="handle-service-control-codes"></a>Verarbeiten von Dienststeuerungscodes

-   Wenn eine Dienststeuerungsmeldung empfangen wird, ruft WDS den [*PxeProviderServiceControl-Rückruf*](pxeproviderservicecontrol.md) auf.
-   Der Anbieter kann eine [*PxeProviderServiceControl-Rückruffunktion*](pxeproviderservicecontrol.md) definieren, um Dienststeuerungsmeldungen zu verarbeiten.
-   Registrieren Sie den [*PxeProviderServiceControl-Rückruf,*](pxeproviderservicecontrol.md) indem Sie während der Verarbeitung des [*PxeProviderInitialize-Rückrufs*](pxeproviderinitialize.md) die [**PxeRegisterCallback-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) mit **PXE \_ CALLBACK \_ SERVICE \_ CONTROL** aufrufen.

## <a name="add-trace-entries-to-pxe-log"></a>Hinzufügen von Ablaufverfolgungseinträgen zum PXE-Protokoll

-   Die [**PxeTrace-Funktion**](/windows/win32/api/WdsPxe/nf-wdspxe-pxetrace) fügt dem PXE-Protokoll einen Ablaufverfolgungseintrag hinzu. WDSPXE bietet Ablaufverfolgung, um Administratoren bei der Problembehandlung zu unterstützen. Anbieter können Ablaufverfolgungseinträge mit unterschiedlichen Schweregraden protokollieren. Die Administratoren können WDSPXE so konfigurieren, dass nur Einträge für bestimmte Schweregrade protokolliert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Windows Deployment Services-API](about-the-windows-deployment-services-api.md)
</dt> <dt>

[Verwenden der Client-API der Windows-Bereitstellungsdienste](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 




