---
title: Verwenden der Client-API der Windows-Bereitstellungsdienste
description: In Umgebungen, in denen Windows-Bereitstellungs Dienste (Windows Deployment Services, WDS) nicht zum Installieren von Windows verwendet werden können, ermöglicht die API des WDS-Clients Entwicklern das Schreiben von benutzerdefinierten Bereitstellungs Anwendungen.
ms.assetid: abe2a7c7-989a-456e-80df-90d5b816db38
keywords:
- Windows-Bereitstellungs Dienste Windows-Bereitstellungs Dienste, verwenden der Client-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 872422a5c84bf1d8ea7c3688b122ba2389c1e968
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039135"
---
# <a name="using-the-windows-deployment-services-client-api"></a>Verwenden der Client-API der Windows-Bereitstellungsdienste

In Umgebungen, in denen Windows-Bereitstellungs Dienste (Windows Deployment Services, WDS) nicht zum Installieren von Windows verwendet werden können, ermöglicht die API des WDS-Clients Entwicklern das Schreiben von benutzerdefinierten Bereitstellungs Anwendungen. Anwendungen können diese API verwenden, um mit dem WDS-Server zu kommunizieren, um Informationen zu System Images zu erhalten, die vom Server zur Verfügung gestellt werden. Benutzerdefinierte WDS-Client Anwendungen sollten die folgenden Richtlinien einhalten.

## <a name="install-the-wds-role-on-the-server"></a>Installieren der WDS-Rolle auf dem Server

-   Bei den Windows-Bereitstellungs Diensten (Windows Deployment Services, WDS) handelt es sich um die überarbeitete Version der Remoteinstallations Dienste (Remote Installation Services, RIS). Sie benötigen die WDS-Server Rolle auf dem Server, um
-   WDS ersetzt RIS als Standardkomponente ab Windows Server 2008 und Windows Server 2003 mit Service Pack 2 (SP2).
-   Sie müssen den RIS-Server auf WDS unter Windows Server 2003 mit Service Pack 1 (SP1) aktualisieren. Sie können die WDS-Server Rolle mit dem [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333)installieren.

## <a name="start-windows-pe-20"></a>Starten von Windows PE 2,0

Windows PE 2,0 muss gestartet werden, wenn es nicht bereits gestartet wurde. Der WDS-Client und die unterstützenden DLLs werden nur durch setup.exe geladen, wenn er sich in der Microsoft Windows Preinstallation Environment-Phase (Windows PE 2,0) der Setup Verarbeitung befindet.

-   Wenn ein neuer Computer mit dem Netzwerk verbunden ist, kann die integrierte PXE (Preboot Execution Environment)-Technologie verwendet werden, um das Netzwerkstart Programm herunterzuladen. Weitere Informationen zum PXE-Start eines Computers für die Installation von Windows finden Sie in [der schrittweisen Anleitung zur Aktualisierung der Windows-Bereitstellungs Dienste](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).
-   Ein RAMDisk-Start fähiges Image von Windows PE 2,0 kann im gespeichert werden. WIM-Format, das als Teil des Netzwerkstart Prozesses heruntergeladen wird. Windows PE kann dann direkt von diesem Medium geladen und ausgeführt werden.

## <a name="open-a-session-with-the-wds-server"></a>Öffnen einer Sitzung mit dem WDS-Server

Der WDS-Client muss eine Sitzung mit einem WDS-Server öffnen.

-   Verwenden Sie die Funktion [**wdsclikreatesession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) , um eine Sitzung mit einem WDS-Server zu öffnen. Diese Funktion nimmt den Namen oder die IP-Adresse des Servers an und empfängt die Adresse des Handles für die WDS-Client Sitzung.
-   Wenn beim Öffnen der Sitzung mit dem Server der WDS-Client authentifiziert werden muss, sollte die Anwendung die Adresse einer [**WDS \_ \_ -CLI-cred-**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred) Struktur mit den Client Anmelde Informationen bereitstellen, wenn die [**wdsclicreatesession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) -Funktion aufgerufen wird. Die Anwendung kann die [**wdscliauthorizesession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliauthorizesession) -Funktion verwenden, um eine anonyme Sitzung in eine authentifizierte Sitzung zu konvertieren.
-   Wenn die mit der [**wdsclicreatesession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) -Funktion geöffnete Sitzung nicht mehr benötigt wird, sollte die Anwendung die [**wdscliclose**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliclose) -Funktion verwenden, um das Handle und die Freigabe Ressourcen zu schließen, die von der Sitzung gehalten werden.

## <a name="enumerate-system-images-on-the-wds-server"></a>Aufzählen von System Images auf dem WDS-Server

Der WDS-Client kann die-API verwenden, um die System Images auf dem WDS-Server aufzuzählen.

-   Verwenden Sie die [**wdsclifindfirstimage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) -Funktion, um ein Handle für das erste Bild abzurufen und die Enumeration von Images auf dem WDS-Server zu initialisieren.
-   Verwenden Sie die [**wdsclifindnextimage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) -Funktion, um die Enumeration zu erhöhen, die von der [**wdsclifindfirstimage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) -Funktion gestartet wurde. Die **wdsclifindnextimage** -Funktion Ruft das Handle für das nächste Bild ab.
-   Verwenden Sie die [**wdscligetimageindex**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageindex) -Funktion, um den Image Index für das aktuelle Bild abzurufen. Dieser Wert ist nur gültig, bis die Funktionen [**wdsclifindnextimage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) oder [**wdscliclose**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliclose) wieder verwendet werden.
-   Verwenden Sie die [**wdscligetenenreerationflags**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetenumerationflags) -Funktion, um informationsflags zur Bildfilterung zu erhalten.

## <a name="get-information-about-images"></a>Informationen zu Images

Der WDS-Client kann die-API verwenden, um Informationen zu den Images auf einem WDS-Server zu erhalten. Mit den folgenden Funktionen werden Informationen zum aktuellen Bild angezeigt. Da die Funktionen [**wdsclifindfirstimage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) und [**wdsclifindnextimage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) den aktuellen Bild handle Wert ändern, sollte die Anwendung alle Informationen speichern, die Sie in der Zukunft erhält und in der Zukunft benötigt, bevor Sie die **wdsclifindfirstimage** -oder **wdsclifindnextimage** -Funktionen erneut aufrufen.

-   Verwenden Sie die [**wdscligetimagetimagetimagetimagetimage-**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagearchitecture) Funktion, um die Prozessorarchitektur
-   Verwenden Sie die [**wdscligetimagepath**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagepath) -Funktion, um den relativen Pfad zur Bilddatei, die das aktuelle Bild enthält, zu erhalten.
-   Verwenden Sie die [**wdscligetimagesize**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagesize) -Funktion, um die Bildgröße zu erhalten.
-   Verwenden Sie die Funktion [**wdscligetimageversion**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageversion) , um die Image Version zu erhalten.
-   Verwenden Sie die [**wdscligetimagelanguage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguage) -Funktion, um die Standardsprache des aktuellen Bilds abzurufen.
-   Verwenden Sie die [**wdscligetimagelanguages**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguages) -Funktion, um ein Array von Sprachen abzurufen, die vom aktuellen Image unterstützt werden.
-   Verwenden Sie [**wdscligetimagelastmodifiedtime**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelastmodifiedtime) gibt die Zeit der letzten Änderung für das aktuelle Bild zurück.
-   Verwenden Sie die [**wdscligetimagename**](/windows/win32/api/WdsClientApi/nf-wdsclientapi-wdscligetimagename) -Funktion, um den Namen des aktuellen Bilds abzurufen.
-   Verwenden Sie die [**wdscligetimagedescription**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagedescription) -Funktion, um die Beschreibung des aktuellen Bilds zu erhalten.
-   Verwenden Sie die Funktion [**wdscligetimagegroup**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagegroup) , um den Image Gruppennamen für das aktuelle Image zu erhalten.
-   Verwenden Sie die Funktion [**wdscligetimagehalname**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehalname) , um den HAL-Namen (Hardware Abstraktion Layer) für das aktuelle Bild zu erhalten.

## <a name="log-wds-client-events"></a>Protokollieren von WDS-Client Ereignissen

Die Protokollierungsfunktionen der WDS-Client Bibliothek ermöglichen das Senden von Installations Fortschritts Ereignissen vom Client an den WDS-Server.

-   Verwenden Sie die [**wdscliinitializelog**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliinitializelog) -Funktion, um das Protokoll für die WDS-Client Sitzung zu initialisieren.
-   Verwenden Sie die [**wdsclilog**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclilog) -Funktion, um Ereignismeldungen in das WDS-Server Protokoll zu schreiben.
-   Unter Windows Server 2008 schreibt der WDS-Server Client Ereignisse in ein anwendungsspezifisches Ereignisprotokoll, das über eventvwr.exe und das Debug-Ablauf Verfolgungs Protokoll angezeigt werden kann. Auf Windows Server 2003 mit aktivierter Debugprotokollierung schreibt der WDS-Server Client Ereignisse in die Protokolldatei unter% windir% \\ Tracing \\ WDSServer. log. Die WDS-Client Protokollierung muss auf dem Server aktiviert sein, um diese Ereignisse zu erfassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur API für die Windows-Bereitstellungs Dienste](about-the-windows-deployment-services-api.md)
</dt> <dt>

[Verwenden der Server-API der Windows-Bereitstellungsdienste](using-the-windows-deployment-services-server-api.md)
</dt> </dl>

 

 