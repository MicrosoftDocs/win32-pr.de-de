---
description: Umgang mit Ären im japanischen Kalender
ms.assetid: a1dabf7c-6521-492e-bdc0-27cfb07cfc20
title: Umgang mit Ären im japanischen Kalender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6ba9c8957bc37a3e200aad546d04629b049dfb3a7962f73d463358d879fb718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949419"
---
# <a name="era-handling-for-the-japanese-calendar"></a>Umgang mit Ären im japanischen Kalender

Viele Kalender weisen Zeiten auf, z. B. AD/BC oder CE/BCE. Im japanischen Kalender werden Jahre durch neng username beschrieben, eine Kombination aus Jahresnummer und Zeitraumname. 2009 ist beispielsweise Heisei 21. In der Vergangenheit haben sich die Namen japanischer Epochen häufig geändert, aber jetzt ändern sich die japanischen Epochen nur bei der Folge nacheinander. Windows und Microsoft .NET haben in der Vergangenheit die vier modernen Epochen unter dieser Richtlinie unterstützt: Jiji, Taishbat, Shwa und Heisei.

Mit Windows 7, Windows Server 2008 R2 und dem .NET Framework 4 erkennt Microsoft, dass in Zukunft weitere Löschzeiten hinzugefügt werden können. In diesen Versionen von Windows werden die Zeitraumdaten in der Registrierung unter dem Schlüssel gespeichert:<dl> HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Nls \\ Calendars \\ Japanese \\ Eras  
</dl>

Bei Bedarf können diesem Schlüssel über den normalen Windows Updateprozess zusätzliche Zeitabstände hinzugefügt werden. Dieser Schlüssel kann mit dem Registrierungs-Editor (Regedit.exe) angezeigt werden. Ein Beispiel für den Schlüssel und die Werte, die in Windows 7 enthalten sind, ist:

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

Der Name jedes Zeitraumwerts ist das Datum, an dem der Zeitraum im gregorianischen Kalender beginnt. Der Wert enthält den Namen der Zeit in Japanisch, den abgekürzten Namen in Japanisch, den Namen in Englisch und einen abgekürzten Namen auf Englisch:<dl> "JJJJ MM TT"="JE \_ AJE \_ EE \_ AEE"  
</dl>where

-   "YYYY MM DD" ist das gregorianische Datum des Beginns der Zeit in Jahr, Monat, Tagformular, wobei Jahr 4 Ziffern, Tag 2 Ziffern und Monat auch 2 Ziffern sind. Ein Leerzeichen trennt jeden Teil des Datums.
-   "JE" ist der japanische Name der Zeit, gefolgt von einem Unterstrich.
-   "AJE" ist der abgekürzte Name der Zeit auf Japanisch, gefolgt von einem Unterstrich.
-   "EE" ist der englische Name der japanischen Zeit, gefolgt von einem Unterstrich.
-   "AEE" ist der abgekürzte englische Name der japanischen Zeit.

Ein Aspekt für Anwendungsentwickler ist die Möglichkeit, dass durch Windows Update oder auf andere Weise weitere Löschzeiten hinzugefügt werden. In diesem Fall kann die Anwendung mehr als die erwarteten vier Epochen für den japanischen Kalender treffen. Zu Testzwecken können Tester der Registrierung einen zusätzlichen Zeitraum hinzufügen. dies sollte jedoch nur auf Testcomputer beschränkt werden, da sich dies auf das Verhalten des gesamten Computers auswirkt.

Ein Beispiel für einen solchen Schlüssel, der für Tests verwendet werden kann, folgt. Diese Änderung kann mit dem Registrierungs-Editor vorgenommen werden. (Dies ist ein Beispiel für die ausschließliche Testverwendung und dient nicht dazu, zukünftige Ergänzungen vorherzusagen.)

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

Beachten Sie, dass sich dies nur auf Computer auswirkt, auf denen Windows 7 und höher oder .NET Framework 4 und höher ausgeführt wird. Anwendungsentwicklern wird empfohlen, ihre Anwendungen mit solchen zusätzlichen Testzeiten zu testen, um sicherzustellen, dass ihre Anwendungen weiterhin funktionieren, wenn zu einem späteren Zeitpunkt weitere Zeitbereiche hinzugefügt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abrufen von Uhrzeit- und Datumsinformationen](retrieving-time-and-date-information.md)
</dt> <dt>

[Kalenderbezeichner](calendar-identifiers.md)
</dt> </dl>

 

 



