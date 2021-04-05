---
title: Verwenden der Server-API der Windows-Bereitstellungsdienste
description: In Umgebungen, in denen die Standardlösung für Windows-Bereitstellungs Dienste (Windows Deployment Services, WDS) nicht verwendet werden kann, macht der WDS-Server eine API verfügbar, die Entwicklern das Schreiben von Plug-ins, die als Anbieter bezeichnet werden, zum Verarbeiten von PXE-Anforderungen (Preboot Execution Environment
ms.assetid: 5e25654a-33c6-4c0f-acc3-e938d1f4a4e7
keywords:
- Windows-Bereitstellungs Dienste Windows-Bereitstellungs Dienste, verwenden der Server-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3634dffa73eddc9b5db92be6bc807cccbc5248f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "103724257"
---
# <a name="using-the-windows-deployment-services-server-api"></a>Verwenden der Server-API der Windows-Bereitstellungsdienste

In Umgebungen, in denen die Standardlösung für Windows-Bereitstellungs Dienste (Windows Deployment Services, WDS) nicht verwendet werden kann, macht der WDS-Server eine API verfügbar, die Entwicklern das Schreiben von Plug-ins, die als Anbieter bezeichnet werden, zum Verarbeiten von PXE-Anforderungen (Preboot Execution Environment Entwickler sollten die folgenden Richtlinien befolgen, wenn Sie PXE-Anbieter für WDS schreiben.

## <a name="install-the-wds-role-on-the-server"></a>Installieren der WDS-Rolle auf dem Server

-   Bei den Windows-Bereitstellungs Diensten (Windows Deployment Services, WDS) handelt es sich um die überarbeitete Version der Remoteinstallations Dienste (Remote Installation Services, RIS). Sie benötigen die WDS-Server Rolle, um den WDS
-   WDS ersetzt RIS als Standardkomponente ab Windows Server 2008 und Windows Server 2003 mit Service Pack 2 (SP2).
-   Sie müssen den RIS-Server auf WDS unter Windows Server 2003 mit Service Pack 1 (SP1) aktualisieren. Sie können die WDS-Server Rolle mit dem [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333)installieren.

## <a name="register-providers"></a>Anbieter registrieren

-   Registrieren Sie die Anbieter-DLL (Dynamic Link Library) während der Installation, und fügen Sie den Anbieter in die geordnete Liste registrierter Anbieter ein.
    > [!Note]  
    > Wenn Sie einen neuen oder geänderten Anbieter installieren, müssen Sie den WDS-PXE-Dienst neu starten, damit die Änderungen wirksam werden.

     

-   Verwenden Sie die [**pxeproviderregister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister) -Funktion, um den Anbieter zu registrieren und der Liste hinzuzufügen. Verwenden Sie die [**pxeproviderunregister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderunregister) -Funktion, um die Registrierung eines registrierten Anbieters aufzuheben und aus der Liste zu entfernen.
-   Geben Sie die Reihenfolge des Anbieters in der geordneten Liste an. Der Index eines Anbieters in der Liste kann nicht garantiert werden, weil ein anderer Anbieter möglicherweise später registriert wird. Um den Anbieter vor oder nach einem anderen registrierten Anbieter in der Liste einzufügen, verwenden Sie zunächst die [**pxeproviderqueryindex**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex) -Funktion, um den Index des registrierten Anbieters zu erhalten, und registrieren Sie dann den neuen Anbieter, während Sie einen größeren oder kleineren Indexwert angeben.
-   Bei der Installation können Anbieter Konfigurationsinformationen unter dem Registrierungsschlüssel gespeichert werden, der zurückgegeben wird, wenn der Anbieter registriert wird. Die Adresse des Registrierungsschlüssels wird vom *phproviderkey* von [**pxeproviderregister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister)empfangen. Der Anbieter erhält ein Handle für denselben Schlüssel wie der *hproviderkey* -Parameter für seinen [*pxeproviderinitialize*](pxeproviderinitialize.md) -Rückruf. Der Anbieter sollte die Adresse dieses Schlüssels speichern.
-   Installieren Sie immer die Anbieter-DLL (Dynamic-Link Library) im Ordner "Programme" des Servers.

## <a name="initialize"></a>Initialisieren

-   Fügen Sie eine DLL ein, die die [*pxeproviderinitialize*](pxeproviderinitialize.md) -Rückruffunktion in den Anbieter exportiert. Jeder Anbieter erfordert einen *pxeproviderinitialize* -Rückruf. Wenn WDS einen Anbieter lädt, ruft er die *pxeproviderinitialize* -Funktion des Anbieters auf und übergibt ein Handle an denselben Schlüssel, der zum Speichern der Konfigurationsinformationen während der Anbieter Registrierung verwendet wird.
-   Wenn der [*pxeproviderinitialize*](pxeproviderinitialize.md) -Rückruf zurückkehrt und erfolgreich ist, sollte der Anbieter vollständig initialisiert und bereit für die Verarbeitung von Anforderungen sein.
-   Registrieren Sie bei der Verarbeitung der [*pxeproviderinitialize*](pxeproviderinitialize.md) -Funktion jeden Rückruf im Anbieter. Rückrufe sollten bei der [**pxeregistercallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion registriert werden.
-   Initialisieren Sie alle internen Ressourcen des Anbieters innerhalb der Verarbeitung der [*pxeproviderinitialize*](pxeproviderinitialize.md) -Funktion.

## <a name="shutdown"></a>Shutdown

-   Implementieren Sie den [*pxeprovidershutdown*](pxeprovidershutdown.md) -Rückruf. Jeder Anbieter muss über einen *pxeprovidershutdown*-Rückruf verfügen.
-   Die [*pxeprovidershutdown*](pxeprovidershutdown.md) -Rückruffunktion sollte den Anbieter vollständig Herunterfahren und alle zugehörigen Ressourcen freigeben.
-   Nachdem der [*pxeprovidershutdown*](pxeprovidershutdown.md) -Rückruf zurückgegeben wurde, ist das an die [*pxeproviderinitialize*](pxeproviderinitialize.md) -Funktion weiter gegebene *hprovider* -Handle nicht mehr gültig und sollte nicht zum Abrufen von WDS verwendet werden.
-   Registrieren Sie den [*pxeprovidershutdown*](pxeprovidershutdown.md) -Rückruf durch Aufrufen der [**pxeregistercallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion mit dem Herunterfahren des **PXE- \_ Rückrufs \_** während der Verarbeitung des [*pxeproviderinitialize*](pxeproviderinitialize.md) -Rückrufs. Rufen Sie den *pxeprovidershutdown* -Rückruf nicht auf, wenn die *pxeproviderinitialize* -Funktion fehlschlägt.

## <a name="handle-request-packet"></a>Anforderungspaket verarbeiten

Implementieren Sie den [*pxeproviderrecvrequest*](pxeproviderrecvrequest.md) -Rückruf für den Anbieter. Jeder Anbieter muss über einen *pxeproviderrecvrequest* -Rückruf verfügen. Wenn WDS eine Anforderung empfängt, ruft er den *pxeproviderrecvrequest* -Rückruf für den ersten Anbieter in der Liste registrierter Anbieter auf.

-   Wenn der Anbieter diese Anforderung synchron verarbeitet, sollte die [*pxeproviderrecvrequest*](pxeproviderrecvrequest.md) -Funktion den Wert **Fehler \_ erfolgreich** zurückgeben. Nur dann, wenn der Anbieter diese Anforderung asynchron verarbeitet, sollte der *pxeproviderrecvrequest* -Rückruf die Fehler-e/a **\_ \_ Ausstehend** zurückgeben und die [**pxeasyncrecvdone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) -Funktion aufzurufen, wenn die Anforderung verarbeitet wurde.
-   Der [*pxeproviderrecvrequest*](pxeproviderrecvrequest.md) -Rückruf und die [**pxeasyncrecvdone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) -Funktion gibt die Adresse einer **PXE- \_ Start \_ Aktions** -Aufzählung zurück, die die vom Anbieter zum Verarbeiten der Anforderung ausgeführte Aktion beschreibt.

    Es gibt vier Möglichkeiten für einen Anbieter, eine Anforderung zu verarbeiten:

    -   Der Anbieter antwortet dem Client mit einem Standard-DHCP-Antwortpaket, das einen Pfad zum Netzwerkstart Programm enthält. Das Zurückgeben des **PXE \_ BA- \_ NBP** -Werts für die Enumeration bedeutet, dass der Anbieter das Anforderungspaket erfolgreich verarbeitet und die Anforderung durch das Senden eines Antwort Pakets durch Aufrufen der Funktionen [**pxepacketallocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) und [**pxesendreply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) abgeschlossen hat.
    -   Der Anbieter antwortet dem Client mit einem benutzerdefinierten Antwortpaket, das nicht DHCP entspricht. Das Zurückgeben des **\_ \_ benutzerdefinierten PXE BA** -Werts für die Enumeration bedeutet, dass der Anbieter das Anforderungspaket erfolgreich verarbeitet und die Anforderung durch das Senden eines benutzerdefinierten Antwort Pakets durch Aufrufen der Funktionen [**pxepacketallocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) und [**pxesendreply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) abgeschlossen hat.
    -   Der Anbieter bestimmt, dass die Anforderung ignoriert werden soll. Durch die Rückgabe des **PXE \_ BA- \_ ignorierwerts** für die Enumeration hat der Anbieter alle Ressourcen freigegeben, die der Anforderung zugeordnet sind, und die Anforderung wird nicht an den nächsten Anbieter in der Liste der registrierten Anbieter übergeben. Anbieter können diese Option verwenden, wenn Sie feststellen, dass ein Anforderungspaket ungültig ist.
    -   Der Anbieter lehnt die Dienst Anforderung ab. Die Rückgabe des **PXE \_ BA- \_ Ablehnungs** Werts für die Enumeration weist das System an, die Anforderung an den nächsten Anbieter in der Liste der registrierten Anbieter zu übergeben. Wenn dies der letzte Anbieter in der Liste wäre, werden alle der Anforderung zugeordneten Ressourcen freigegeben, und die Anforderung wird ignoriert.
    -   Registrieren Sie den [*pxeproviderrecvrequest*](pxeproviderrecvrequest.md) -Rückruf durch Aufrufen der [**pxeregistercallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion mit **PXE \_ Callback \_ recv \_ Request** während der Verarbeitung des [*pxeproviderinitialize*](pxeproviderinitialize.md) -Rückrufs.

## <a name="generate-response-packet"></a>Antwortpaket generieren

-   Verwenden Sie die API zum Schreiben von Anbietern, um die DHCP-Anforderung zu verarbeiten und Antwort Pakete zu generieren.
-   Die [**pxeprovidersetattribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) -Funktion gibt die Attribute an, die vom Anbieter zum Filtern von Paketen verwendet werden. Die Attribute des Anbieters können so angegeben werden, dass der Anbieter alle Pakete sieht, der Anbieter nur DHCP-Pakete erkennt oder der Anbieter nur DHCP-Pakete erkennt, die die DHCP-Anbieter Klassen-Bezeichneroption (60) als "PXEClient" angeben.
-   Die [**pxedhcpisvalid**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpisvalid) -Funktion überprüft, ob ein Paket ein gültiges DHCP-Paket ist. Anbieter können die **pxedhcpisvalid** -Funktion verwenden, um zu überprüfen, ob ein Paket vom Client ein DHCP-Paket ist, wenn der Filtersatz mit der [**pxeprovidersetattribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) -Funktion auf den Empfang aller Pakete festgelegt ist, um zu bestimmen, ob ein bestimmtes Paket ein gültiges DHCP-Paket ist.
-   Die [**pxedhcpinitialize**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpinitialize) -Funktion initialisiert ein Antwortpaket als DHCP-Antwortpaket, das auf den Informationen in einem Paket basiert, das vom Client empfangen wurde. Die [*pxeproviderinitialize*](pxeproviderinitialize.md) -Funktion nimmt die Adresse eines gültigen DHCP-Pakets an, das vom Client im [*pxeproviderrecvrequest*](pxeproviderrecvrequest.md) -Rückruf empfangen wurde. Die **pxedhcpinitialize** -Funktion nimmt einen Zeiger auf ein Antwortpaket an, das der [**pxepacketallocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) -Funktion zugeordnet ist.
-   Die [**pxedhcpgetoptionvalue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue) -Funktion Ruft einen Optionswert aus einem DHCP-Paket ab. Die [**pxedhcpgetvendoroptionvalue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) -Funktion Ruft einen Optionswert aus dem herstellerspezifischen Informationsfeld (43) eines DHCP-Pakets ab.
-   Der Anbieter kann dann das Antwortpaket mit Informationen auffüllen und die [**pxesendreply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) -Funktion verwenden, um das Antwortpaket an den Client zu senden. Die [**pxedhcpappdoption**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpappendoption) -Funktion fügt eine DHCP-Option an das Antwortpaket an.
-   Ein Anbieter, der auf Client Anforderungen durch das Senden eines Pakets antwortet, muss das Antwortpaket mithilfe der [**pxepacketallocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) -Funktion zuordnen. Der Anbieter kann dann das Antwortpaket mit Informationen auffüllen und die [**pxesendreply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) -Funktion verwenden, um das Antwortpaket an den Client zu senden.
-   Wenn der zugeordnete Arbeitsspeicher nicht mehr benötigt wird, sollte der Anbieter ihn mithilfe der [**pxepacketfree**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketfree) -Funktion freigeben.

## <a name="enumerate-registered-providers"></a>Registrierte Anbieter aufzählen

-   Verwenden Sie die-API zum Schreiben von Anbietern, die andere registrierte Anbieter in der Liste aufzählen und überprüfen.
-   Die [**pxegetserverinfo**](/windows/win32/api/WdsPxe/nf-wdspxe-pxegetserverinfo) -Funktion gibt Informationen über den PXE-Server zurück. Die **pxegetserverinfo** -Funktion gibt einen **booleschen** Wert zurück, der angibt, ob die Ablauf Verfolgung für den Server aktiviert ist. **True** gibt an, dass die Ablauf Verfolgung aktiviert ist.
-   Die [**pxeproviderenumfirst**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst) -Funktion startet eine enumerationof-Anbieter in der Liste registrierter Anbieter. Die **pxeproviderenumfirst** -Funktion startet die-Enumeration und gibt die Adresse des Handles zurück, das beim Aufrufen der [**pxeproviderenumnext**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumnext) -Funktion verwendet werden soll. Die **pxeproviderenumnext** -Funktion gibt eine [**PXE- \_ Anbieter**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider) Struktur zurück, die die Informationen zum Anbieter enthält. Die [**pxeproviderfreone FO**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo) -Funktion gibt den Arbeitsspeicher frei, der der **PXE- \_ Anbieter** Struktur von der **pxeproviderenumnext** -Funktion zugeordnet wurde. Die [**pxeproviderenumclose**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumclose) -Funktion schließt die Enumeration von Anbietern in der Liste der registrierten Anbieter.

## <a name="handle-service-control-codes"></a>Verarbeiten von Dienst Steuerungs Codes

-   Wenn eine Dienst Steuerungs Meldung empfangen wird, ruft WDS den [*pxeproviderservicecontrol*](pxeproviderservicecontrol.md) -Rückruf auf.
-   Der Anbieter kann eine [*pxeproviderservicecontrol*](pxeproviderservicecontrol.md) -Rückruffunktion definieren, um Dienst Steuerungs Meldungen zu verarbeiten.
-   Registrieren Sie den [*pxeproviderservicecontrol*](pxeproviderservicecontrol.md) -Rückruf durch Aufrufen der [**pxeregistercallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion mit dem **PXE- \_ Rückruf \_ Dienst- \_ Steuer** Element während der Verarbeitung des [*pxeproviderinitialize*](pxeproviderinitialize.md) -Rückrufs.

## <a name="add-trace-entries-to-pxe-log"></a>Ablauf Verfolgungs Einträge zum PXE-Protokoll hinzufügen

-   Die [**pxetrace**](/windows/win32/api/WdsPxe/nf-wdspxe-pxetrace) -Funktion fügt dem PXE-Protokoll einen Ablauf Verfolgungs Eintrag hinzu. Wdspxe bietet eine Ablauf Verfolgung, die Administratoren bei der Problembehandlung unterstützt. Anbieter können Ablauf Verfolgungs Einträge verschiedener Schweregrade protokollieren. Die Administratoren können wdspxe so konfigurieren, dass nur Einträge für bestimmte Schweregrade protokolliert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur API für die Windows-Bereitstellungs Dienste](about-the-windows-deployment-services-api.md)
</dt> <dt>

[Verwenden der Client-API der Windows-Bereitstellungsdienste](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 




