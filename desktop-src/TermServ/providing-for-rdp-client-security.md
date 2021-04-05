---
title: Bereitstellen der RDP-Client Sicherheit
description: Einige Eigenschaften des Remotedesktop ActiveX-Steuerelement Objekts sind auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt.
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15bbb143abd3ec09a7f1aeff67a7b6dfa224b56b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710187"
---
# <a name="providing-for-rdp-client-security"></a>Bereitstellen der RDP-Client Sicherheit

Um es Clients zu ermöglichen, sich selbst vor potenziell nicht vertrauenswürdigen Servern zu schützen, werden einige Eigenschaften des Remotedesktop ActiveX-Steuerelement Objekts auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt. Dies bedeutet Folgendes: Wenn ein Benutzer, der das Internet durchsucht, auf die Seite zugreift und sich die Seite in einer höheren URL-Sicherheitszone als der Computer befindet, mit dem Sie das Web durchsuchen, sind diese Eigenschaften deaktiviert. Auf diese eingeschränkten Eigenschaften wird mithilfe der [**imstscsecuredsettings**](imstscsecuredsettings-interface.md) -Schnittstelle und der [**imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md) -Schnittstelle zugegriffen, und Sie sind in den folgenden Sicherheitszonen für Internet Explorer-URLs verfügbar:

-   Arbeitsplatz
-   Lokales Intranet
-   Vertrauenswürdige Sites

Sie sind in diesen Zonen deaktiviert:

-   Internet
-   Eingeschränkte Websites

Wenn Sie diese eingeschränkten Eigenschaften in der Remotedesktopdienste-Webanwendung aufrufen, sollten Sie [**imstscax:: get \_ securedsettings**](imstscax-securedsettings.md) und [**imstscax:: get \_ securedsettingsenabled**](imstscax-securedsettingsenabled.md) aufrufen, um auf die Eigenschaften der gesicherten Einstellungen zuzugreifen.

Die eingeschränkten Eigenschaften, auf die die **imstscsecuredsettings** -Schnittstelle zugreift, lauten wie folgt:

-   [**StartProgram**](imstscsecuredsettings-startprogram.md). Diese Eigenschaft gibt das Programm an, das bei der Verbindung gestartet wird.
-   [**WorkDir**](imstscsecuredsettings-workdir.md). Diese Eigenschaft gibt das Arbeitsverzeichnis des Programms an, das in [**StartProgram**](imstscsecuredsettings-startprogram.md)angegeben ist.
-   [**Vollbild**](imstscsecuredsettings-fullscreen.md). Diese Eigenschaft gibt an, ob sich der Zustand des Steuer Elements bei der Verbindung im Vollbildmodus oder im Fenstermodus befindet. Wenn der Wert dieser Eigenschaft **true** ist, wird die Verbindung im Vollbildmodus geöffnet. Obwohl die Verwendung der **Fullscreen** -Eigenschaft auf die zuvor aufgeführten Internet Explorer-URL-Sicherheitszonen beschränkt ist, kann ein Benutzer nach der Verbindungs Herstellung jederzeit in den Vollbildmodus wechseln, indem er die [Tasten](terminal-services-shortcut-keys.md) Kombination für den Vollbildmodus (Strg + Alt + untbuggung) drückt.

Die Eigenschaften, auf die die **imsrdpclientsecuredsettings** -Schnittstelle zugreift, lauten wie folgt:

-   [**Audioredirectionmode**](imsrdpclientsecuredsettings-autoredirectionmode.md). Diese Eigenschaft gibt an, ob Sounds umgeleitet oder Sounds auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) abgespielt werden.
-   [**Keyboardhuokmode**](imsrdpclientsecuredsettings-keyboardhookmode.md). Diese Eigenschaft gibt an, wie und wann Windows-Tastenkombinationen angewendet werden sollen. Beispiel: Alt + Tab.

Mit dem folgenden Skript wird Microsoft Notepad.exe bei der Verbindung gestartet. Führen Sie dieses Skript aus, bevor Sie die [**imstscax:: Connect**](imstscax-connect.md) -Methode aufrufen.

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 




