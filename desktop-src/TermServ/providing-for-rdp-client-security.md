---
title: Bereitstellen von RDP-Clientsicherheit
description: Einige Eigenschaften des Remotedesktop ActiveX-Steuerelementobjekts sind auf bestimmte URL Internet Explorer-Sicherheitszonen beschränkt.
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdcfbc2b26363ff7f13ed15b3486249aab804cd1bde418f60d71db918f25567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117940614"
---
# <a name="providing-for-rdp-client-security"></a>Bereitstellen von RDP-Clientsicherheit

Damit clients sich vor potenziell nicht vertrauenswürdigen Servern schützen können, sind einige Eigenschaften des Remotedesktop ActiveX-Steuerelementobjekts auf bestimmte url Internet Explorer Sicherheitszonen beschränkt. Dies bedeutet, dass diese Eigenschaften deaktiviert sind, wenn ein Benutzer, der im Web auf die Seite zufingt und sich in einer höheren URL-Sicherheitszone befindet als der Computer, mit dem er im Web browset, sich befindet. Der Zugriff auf diese eingeschränkten Eigenschaften erfolgt über die [**IMsTscSecuredSettings-Schnittstelle**](imstscsecuredsettings-interface.md) und die [**IMsRdpClientSecuredSettings-Schnittstelle**](imsrdpclientsecuredsettings-interface.md) und ist in den folgenden URL Internet Explorer Sicherheitszonen verfügbar:

-   Mein Computer
-   Lokales Intranet
-   Vertrauenswürdige Sites

Sie sind in den folgenden Zonen deaktiviert:

-   Internet
-   Eingeschränkte Websites

Wenn Sie diese eingeschränkten Eigenschaften in Ihrer Remotedesktopdienste-Webanwendung aufrufen, sollten Sie [**IMsTscAx::get \_ SecuredSettings**](imstscax-securedsettings.md) und [**IMsTscAx::get \_ SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) aufrufen, um auf die Eigenschaften von Secured Einstellungen zu zugreifen.

Die eingeschränkten Eigenschaften, auf die die **IMsTscSecuredSettings-Schnittstelle** zuweist, sind die folgenden:

-   [**StartProgram**](imstscsecuredsettings-startprogram.md). Diese Eigenschaft gibt das Programm an, das bei der Verbindung gestartet wird.
-   [**WorkDir**](imstscsecuredsettings-workdir.md). Diese Eigenschaft gibt das Arbeitsverzeichnis des in [**StartProgram angegebenen Programms an.**](imstscsecuredsettings-startprogram.md)
-   [**FullScreen**](imstscsecuredsettings-fullscreen.md). Diese Eigenschaft gibt an, ob sich der Zustand des Steuerelements bei der Verbindung im Vollbild- oder Fenstermodus befindet. Wenn der Wert dieser Eigenschaft **TRUE** ist, wird die Verbindung im Vollbildmodus geöffnet. Obwohl die Verwendung der **FullScreen-Eigenschaft** auf die oben aufgeführten Internet Explorer-URL-Sicherheitszonen beschränkt ist, kann ein Benutzer nach [](terminal-services-shortcut-keys.md) der Verbindung immer in den Vollbildmodus wechseln, indem er die Tastenkombination für den Vollbildmodus (STRG+ALT+BREAK) drückt.

Die **IMsRdpClientSecuredSettings-Schnittstelle** hat folgende Eigenschaften:

-   [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md). Diese Eigenschaft gibt an, ob Sounds umgeleitet oder auf dem Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) wiedergibt.
-   [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md). Diese Eigenschaft gibt an, wie und wann sie Windows Tastenkombinationen anwenden soll. Beispiel: ALT+TAB.

Mit dem folgenden Skript wird microsoft Notepad.exe bei der Verbindung gestartet. Führen Sie dieses Skript aus, bevor Sie [**die IMsTscAx::Verbinden**](imstscax-connect.md) aufrufen.

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 




