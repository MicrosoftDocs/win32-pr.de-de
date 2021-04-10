---
description: Ermöglicht Benutzern das Ausführen allgemeiner Aufgaben als nicht-Administratoren, die als Standardbenutzer bezeichnet werden, und als Administratoren, ohne dass Benutzer gewechselt, sich abmelden oder Ausführen als verwendet werden müssen.
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: Benutzerkontensteuerung (Autorisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7f3cd8f31dda8f1b15145bc4003fc9ede8782c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960470"
---
# <a name="user-account-control-authorization"></a>Benutzerkontensteuerung (Autorisierung)

Mithilfe der Benutzerkontensteuerung (User Account Control, UAC) können Benutzer häufig verwendete Aufgaben als nicht Administratoren, als Standardbenutzer bezeichnet, und als Administratoren ausführen, ohne dass Benutzer gewechselt, sich abmelden oder **Ausführen als** verwendet werden müssen. Durch das Verhalten der Benutzerkontensteuerung für die Einstellung "nie Benachrichtigen" wird die UAC nicht mehr deaktiviert. Die Einstellung "nie Benachrichtigen" gibt Ihnen ein geteiltes Token und erhöht immer automatisch die erforderlichen Berechtigungen. Diese Feinheit kann dazu führen, dass Ihre APP Kompatibilitätsprobleme hat. Sie können die Benutzerkontensteuerung weiterhin mithilfe von Gruppenrichtlinien oder manuell durch Festlegen des Registrierungsschlüssels deaktivieren.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Durch die Einstellung "nie Benachrichtigen" wird die UAC deaktiviert.

Wenn Sie z. b. die folgenden Schritte ausführen, um die Einstellung "nie Benachrichtigen" zu ändern, erhalten Sie unterschiedliche Ergebnisse, wenn Sie versuchen, eine Datei in einem Ordner zu erstellen, für den erhöhte Rechte erforderlich sind. Das Verhalten von Windows 8 besteht darin, den Zugriff zu verweigern. Mit dem Windows 7-Verhalten können Sie die File.txt Datei erstellen.

1.  Klicken oder tippen Sie auf **Start**. Geben Sie im Suchfeld "Benutzerkonten Steuerungseinstellungen ändern" ein.
2.  Klicken oder tippen Sie auf **Einstellungen der Benutzerkontensteuerung ändern** , um Sie zu öffnen.
3.  Verschieben Sie den Schieberegler auf **nie Benachrichtigen**.
4.  Klicken oder tippen Sie auf **OK**.
5.  Starten Sie den Computer neu.
6.  Klicken oder tippen Sie auf **Start** und dann auf **Ausführen**. Geben Sie im Feld **Öffnen** den Namen "Cmd.exe" ein. Beachten Sie, dass der Titel des Fensters nicht die Zeichenfolge "Administrator" enthält.
7.  Geben Sie "Echo >% windir% \\ system32 \\File.txt" ein.

UAC wurde in Windows Server 2008 und Windows Vista hinzugefügt. Ein Standardbenutzer Konto ist mit einem Benutzerkonto in Windows XP Synonym. Benutzerkonten, die Mitglieder der lokalen Administrator Gruppe sind, führen die meisten Anwendungen als Standardbenutzer aus.

Weitere Informationen zu UAC finden Sie in den folgenden Themen.



| Thema                                                                                                                                        | BESCHREIBUNG                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Richtlinien für die Benutzerkontensteuerung in der Benutzeroberflächen Entwicklung](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)<br/> | Allgemeine Informationen zu UAC.<br/>                                                                                                     |
| [Entwickeln von Anwendungen, für die Administrator Rechte erforderlich sind](developing-applications-that-require-administrator-privilege.md)<br/>  | Modelle zum Entwickeln von Anwendungen, die Vorgänge ausführen, für die Administrator Berechtigungen erforderlich sind, die jedoch als Standardbenutzer ausgeführt werden.<br/> |
| [Autorisierungs Verweis](authorization-reference.md)<br/>                                                                            | Ausführliche Informationen zu Autorisierungs Funktionen, Schnittstellen, Strukturen und anderen Programmier Elementen.<br/>                        |



 

 

 




