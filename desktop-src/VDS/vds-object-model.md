---
description: VDS-Objektmodell
ms.assetid: e5fcc19a-e170-4918-85eb-c1457776795a
title: VDS-Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae998955c5d0b7834cf4d88b901537f3644a2ab
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104218902"
---
# <a name="vds-object-model"></a>VDS-Objektmodell

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

VDS bietet indirekten Zugriff auf Host basierte Speichergeräte, z. b. Datenträger und CD-ROM-Geräte, sowie auf Datenträger Arrays, die von Hardware-RAID-Controllern verwaltet werden. Während einige Speicher Entitäten physische Geräte modellieren, sind andere Modell-VM-Konstrukte: Volumes, Partitionen usw. Die in diesem Thema beschriebenen Objekte stellen die physischen und virtuellen Entitäten von VDS dar.

Anwendungen rufen die Methoden auf, die von diesen Objekten verfügbar gemacht werden, und VDS Ruft den entsprechenden Anbieter auf, um die angeforderten Speichervorgänge auszuführen. Eine Anwendung ruft ein Anbieter Programm niemals direkt auf.

### <a name="classification-of-objects"></a>Klassifizierung von Objekten

Wie die folgende Abbildung zeigt, implementieren Softwareanbieter Programme Objekte, die Host basierte Entitäten modellieren. Hardware Anbieter Programme implementieren Objekte, die interne und externe Hardware-RAID-Geräte modellieren. die verbleibenden allgemeinen Objekte sind entweder Anbieter unabhängig oder werden von VDS implementiert. Eine Spindel, bei der es sich nicht um ein VDS-Objekt handelt, ist ein Begriff für generische Speichermedien, die aus Datenträger-oder Laufwerks Blöcken bestehen.

![Diagramm, das eine Klassifizierung von Objekten anzeigt, die als "Common Objects", "Software Provider Objects" und "Hardware Provider Objects" definiert sind.](images/vdsobjectmodel.png)

Weitere Informationen zum Verhalten der einzelnen Objekte finden Sie unter den folgenden Themen:

-   Dienst Lade-und Dienst Objekte finden Sie unter [Start-und Dienst Objekte](startup-and-service-objects.md).
-   Zu Enumerations-und asynchronen Objekten finden Sie unter [Helper-Objekte](helper-objects.md)
-   Anbieter Objekt finden Sie unter [Provider Object](provider-object.md).
-   Zu Paket-, Datenträger-, Volume-und volumeplex-Objekten finden Sie unter [Software Provider Objects](software-provider-objects.md).
-   Zu den Objekten Subsystem, Controller, Laufwerk, LUN und LUN Plex finden Sie unter [Hardware Anbieter Objekte](hardware-provider-objects.md).

### <a name="object-creation"></a>Objekterstellung

Die Konfigurations-und Abfrage Vorgänge, die mit der Objekt Erstellung verknüpft sind, können viel Zeit in Anspruch nehmen. Daher ruft VDS alle Methoden asynchron auf. Der Ermittlungs Anbieter gibt alle Abschluss-, Fehler-oder Status Änderungs Ereignisse zurück. Software Anbieter protokollieren außerdem alle Fehler und erheblichen Zustandsänderungen.

### <a name="object-deletion"></a>Löschen von Objekten

Mit mehreren VDS-Methoden werden VDS-Objekte gelöscht oder transformiert. Ein Aufrufer kann einen Verweis über einen Schnittstellen Zeiger auf ein gelöschtes Objekt speichern, nachdem die Methode zurückgegeben wurde. Wenn der Aufrufer die-Schnittstelle freigibt, löscht VDS das-Objekt.

Im Hinblick auf das Löschen von Objekten sollten Aufrufer keine Ausnahme von der [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für diese Schnittstellen aufrufen. Der Anbieter muss robust genug sein, um mit fehlgeleiteten-Aufrufern zu umgehen. Wenn ein Aufrufer eine Methode für ein gelöschtes Objekt aufruft, sollte der Anbieter das **VDS \_ E- \_ Objekt \_ gelöscht** zurückgeben.

### <a name="service-initialization"></a>Dienstinitialisierung

VDS stellt einen Klassen Bezeichner (CLSID) für das Dienst Lade Programm und die Dienst Objekte bereit, aber nur die Dienst Lade Programm-CLSID ist öffentlich. Die Dienst Initialisierung tritt auf, wenn die Anbieter, eine aufrufenden Anwendung und der Dienst die folgenden Aufgaben ausführen:

-   Jeder neue Anbieter ruft während der Installation die [**ivdsadmin:: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) -Methode auf, um sich bei VDS zu registrieren. Der-Befehl erstellt einen Registrierungsschlüssel unter der System Struktur, der durch die Objekt-GUID des Anbieters gekennzeichnet ist. Unter diesem Schlüssel ist die CLSID des Anbieter Objekts, der Name, die Version und die Versions-GUID des Anbieters enthalten.
    > [!Note]  
    > Anbieter Objekt-GUIDs sind persistent. die Software-und Hardware Objekt-GUIDs sind nicht.

     

-   Eine Anwendung ruft die [**cokreatzustance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion auf und übergibt die Dienst Ladefunktion CLSID als Argument. Mit einem Zeiger auf das Service Loader-Objekt kann die Anwendung VDS entweder lokal oder Remote starten, indem der gewünschte Computername als Parameter an die [**ivdsserviceloader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) -Methode übergeben wird.
-   Wenn die anfängliche Anwendung an den Dienst angefügt wird, ruft VDS zuerst [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) für jede CLSID auf, die unter dem Registrierungsschlüssel gefunden wurde, und ruft dann die [**ivdsproviderprivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) -Methode für jeden Anbieter auf, um die Programme zu initialisieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu VDS](about-vds.md)
</dt> <dt>

[**Ivdsadmin:: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider)
</dt> <dt>

[**Ivdsserviceloader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[**Ivdsproviderprivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> </dl>

 

 
