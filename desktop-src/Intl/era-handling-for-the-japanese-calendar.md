---
description: Umgang mit Ären im japanischen Kalender
ms.assetid: a1dabf7c-6521-492e-bdc0-27cfb07cfc20
title: Umgang mit Ären im japanischen Kalender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eba757745bf0d90d119c821772c7fc23f3f8694b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867927"
---
# <a name="era-handling-for-the-japanese-calendar"></a>Umgang mit Ären im japanischen Kalender

Viele Kalender haben Zeiträume, z. b. AD/BC oder CE/BCE. Im japanischen Kalender werden Jahre durch Nengō, eine Kombination aus Jahr-und Zeit Namen, beschrieben. 2009 ist z. b. Heisei 21. In der Vergangenheit haben sich die Namen japanischer Zeiträume häufig geändert, aber jetzt ändern sich die japanischen Zeiträume nur in der kaiserlichen Nachfolge. Windows und Microsoft .net haben in der Vergangenheit vier moderne Zeiträume unter dieser Richtlinie unterstützt: Meiji, Taishō, Shōwa und heiist.

Mit Windows 7, Windows Server 2008 R2 und dem .NET Framework 4 erkennt Microsoft, dass weitere Zeiträume in Zukunft hinzugefügt werden können. In diesen Versionen von Windows werden die ERA-Daten in der Registrierung unter dem Schlüssel gespeichert:<dl> HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ nls \\ Kalenders \\ Japanese \\ Eras  
</dl>

Gegebenenfalls können dem Schlüssel durch den normalen Windows Update Prozess weitere Zeiträume hinzugefügt werden. Dieser Schlüssel kann mithilfe des Registrierungs-Editors (Regedit.exe) angezeigt werden. Ein Beispiel für den in Windows 7 gelieferten Schlüssel und die folgenden Werte sind:

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

Der Name jedes ERA-Werts ist das Datum, an dem der Zeitraum im gregorianischen Kalender beginnt. Der Wert enthält den Zeit Namen in Japanisch, den abgekürzten Namen in Japanisch, den Namen in englischer Sprache und einen abgekürzten Namen in englischer Sprache:<dl> "yyyy mm dd" = "je \_ AJE \_ EE \_ AEE"  
</dl>where

-   "Yyyy mm dd" ist das gregorianische Datum des Zeitraums in Jahr, Monat, Tag, wobei Jahr vier Ziffern, Tag 2 Ziffern und Monat auch 2 Ziffern sind. Die einzelnen Teile des Datums werden durch ein Leerzeichen voneinander getrennt.
-   "Je" ist der japanische Name des Zeitraums, gefolgt von einem Unterstrich.
-   "AJE" ist der abgekürzte Name des Zeitraums, in Japanisch und gefolgt von einem Unterstrich.
-   "Ee" ist der englische Name des japanischen Zeitraums, gefolgt von einem Unterstrich.
-   "AEE" ist der abgekürzte englische Name des japanischen Zeitraums.

Ein Aspekt für Anwendungsentwickler ist die Möglichkeit, dass zusätzliche Zeiträume Windows Update oder auf andere Weise hinzugefügt werden. In diesem Fall kann es sein, dass die Anwendung mehr als die erwarteten vier Zeiträume für den japanischen Kalender trifft. Für Testzwecke können Tester der Registrierung einen zusätzlichen Zeitraum hinzufügen. Dies sollte jedoch nur auf Testcomputer beschränkt werden, da sich dies auf das Verhalten des gesamten Computers auswirkt.

Ein Beispiel für einen solchen Schlüssel, der für Tests verwendet werden kann. Diese Änderung kann mit dem Registrierungs-Editor vorgenommen werden. (Dies ist ein Beispiel für die Test Verwendung, und es ist nicht dafür vorgesehen, zukünftige Ergänzungen vorherzusagen.)

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

Beachten Sie, dass sich dies nur auf Computern mit Windows 7 und höher oder .NET Framework 4 und höher auswirkt. Anwendungsentwicklern wird empfohlen, Ihre Anwendungen mit solchen zusätzlichen Testperioden zu testen, um sicherzustellen, dass Ihre Anwendungen weiterhin funktionieren, wenn zu einem späteren Zeitpunkt weitere Zeiträume hinzugefügt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abrufen von Zeit-und Datumsinformationen](retrieving-time-and-date-information.md)
</dt> <dt>

[Kalender Bezeichner](calendar-identifiers.md)
</dt> </dl>

 

 



