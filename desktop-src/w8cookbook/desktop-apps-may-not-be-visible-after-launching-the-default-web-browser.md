---
title: Desktop-Apps sind nach dem Start der Standard Webbrowser-oder Windows Store-Apps möglicherweise nicht sichtbar.
description: Desktop-Apps sind nach dem Start der Standard Webbrowser-oder Windows Store-Apps möglicherweise nicht sichtbar.
ms.assetid: 5D2CE14B-111D-4987-A9AA-B04AC030F9F0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c80541a860bd29f207ab99eba6ab4cb629a666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104316581"
---
# <a name="desktop-apps-may-not-be-visible-after-launching-the-default-web-browser-or-windows-store-apps"></a>Desktop-Apps sind nach dem Start der Standard Webbrowser-oder Windows Store-Apps möglicherweise nicht sichtbar.

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

Die Benutzeroberfläche der Windows Store-App konzentriert sich auf eine einzelne APP gleichzeitig mit Multitasking, App-Umschaltung und Benachrichtigungen, die von der Windows-Benutzeroberfläche bereitgestellt werden. Für Windows Store-Apps ist die Größenanpassung des verfügbaren Speicherplatzes auf dem Bildschirm mit der gängigsten Ansicht Vollbild verfügbar. Wenn eine andere APP auf dem System gestartet wird, können Sie daher nicht mehr davon ausgehen, dass die neue app in einem Desktop Fenster neben ihrer Desktop-App geöffnet wird. Dies gilt immer für Windows Store-Apps und Browser, die an der neuen Benutzeroberfläche der Windows-Benutzeroberfläche teilnehmen möchten. Möglicherweise werden weitere apps gleichzeitig angezeigt, z. b. Wenn Sie sich auf dem Desktop befinden und eine andere Desktop Anwendung starten oder Anwendungen einen Ansichts Zustand haben.

## <a name="manifestation"></a>Ausstrahlung

Wenn eine Desktop-App gängige Aktivierungsverfahren für die APP verwendet, wie z. b. die Verwendung der ShellExecute-API für eine Datei oder ein Protokoll, wird die dieser Registrierung zugeordnete APP von Windows gestartet. dabei kann es sich um eine Windows Store-App und/oder den Standard Webbrowser des Benutzers handeln. Windows Store-Apps werden im Vollbildmodus gestartet, wobei der Desktop und die Desktop-App, von der Sie gestartet wurde, ausgeblendet werden.

> [!Note]  
> In Windows 8 ist Internet Explorer 10 als Standardbrowser des Benutzers konfiguriert, aber der Benutzer kann sich dafür entscheiden, einen anderen Browser als Standard zu installieren und festzulegen (keine Änderung von Windows 7). Wenn in Internet Explorer 10 ein Link über eine Desktop Anwendung geöffnet wird, wird Internet Explorer auf dem Desktop geöffnet. Diese Einstellung kann jedoch von Benutzern geändert werden, sodass Internet Explorer als Windows Store-App geöffnet wird. Browser Hersteller wurden empfohlen, eine ähnliche "kontextbezogene Start"-Funktion zu verwenden. Entwickler sollten jedoch die Tatsache planen, dass sich nicht alle Browser ähnlich verhalten.

 

## <a name="mitigation"></a>Minderung

Obwohl es keine Änderungen gibt, die Entwickler an Ihren Apps vornehmen können, um dieses Verhalten zu mindern, können die Endbenutzer mit Ihnen kommunizieren. Verwenden Sie ggf. die von der erweiterten ShellExecuteEx ()-API gesammelten Informationen zum Auffüllen eines Kontext gerechten Dialog Felds. Geben Sie in diesem Dialogfeld dem Benutzer an, welche App gestartet werden soll und ob es sich bei dieser APP um eine Windows Store-App oder eine Desktop-App handelt. Die CLSID kann verwendet werden, um Windows Store-Apps von Desktop-Apps zu unterscheiden. Benutzeroptionen:

-   Benutzer mit einem breit Bild Monitor können die Windows Store-App an den Bildschirmrand ausrichten, um den Desktop verfügbar zu machen und so die Windows Store-App und die Desktop-App gleichzeitig anzuzeigen.
-   Wenn Internet Explorer als Standardbrowser des Benutzers konfiguriert ist, können Benutzer das Verhalten ändern, indem Sie die Internet Optionen in der Systemsteuerung ändern. Auf der Registerkarte Programme können Benutzer die Verknüpfungen von Internet Explorer ändern. Andere Browser bieten möglicherweise eine ähnliche Einstellung.

 

 




