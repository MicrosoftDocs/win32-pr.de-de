---
description: Ermöglicht Es Benutzern, allgemeine Aufgaben als Nichtadministratoren, als Standardbenutzer bezeichnet, und als Administratoren auszuführen, ohne Benutzer wechseln, sich abmelden oder Ausführen als verwenden zu müssen.
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: Benutzerkontensteuerung (Autorisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da0092ed5d8de1c141ba4ee2ea31a498bd6954ba8401aafeb08e6a69b8d130f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906830"
---
# <a name="user-account-control-authorization"></a>Benutzerkontensteuerung (Autorisierung)

Mit der Benutzerkontensteuerung (User Account Control, UAC) können Benutzer allgemeine Aufgaben als Nichtadministratoren, als Standardbenutzer und als Administratoren ausführen, ohne benutzerwechseln, abmelden oder ausführen als verwenden **zu müssen.** Das Verhalten der UAC für die Einstellung "Nie benachrichtigen" deaktiviert die UAC nicht mehr. Mit der Einstellung "Nie benachrichtigen" erhalten Sie ein geteiltes Token und erhöhen immer automatisch die erforderlichen Berechtigungen. Diese Feinheiten können dazu führen, dass Ihre App Kompatibilitätsprobleme hat. Sie können die UAC weiterhin deaktivieren, indem Sie Gruppenrichtlinien verwenden oder den Registrierungsschlüssel manuell festlegen.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Die Einstellung "Nie benachrichtigen" deaktiviert die UAC.

Wenn Sie beispielsweise die folgenden Schritte ausführen, um die Einstellung "Nie benachrichtigen" zu ändern, erhalten Sie unterschiedliche Ergebnisse, wenn Sie versuchen, eine Datei in einem Ordner zu erstellen, der erhöhte Rechte erfordert. Das Windows 8 besteht im Verweigern des Zugriffs. Mit Windows 7-Verhalten können Sie die File.txt erstellen.

1.  Klicken oder tippen Sie **auf Starten.** Geben Sie im Suchfeld "Einstellungen der Benutzerkontensteuerung ändern" ein.
2.  Klicken oder tippen **Sie auf Einstellungen der Benutzerkontensteuerung ändern,** um sie zu öffnen.
3.  Verschieben Sie den Schieberegler auf **Nie benachrichtigen.**
4.  Klicken oder tippen Sie **auf OK.**
5.  Starten Sie den Computer neu.
6.  Klicken oder tippen **Sie auf Starten** und dann auf **Ausführen.** Geben Sie **im** Feld Öffnen den Text "Cmd.exe" ein. Beachten Sie, dass der Titel des Fensters nicht die Zeichenfolge "Administrator" enthält.
7.  Geben Sie "echo > %windir% \\ system32 \\File.txt" ein.

UAC wurde in Windows Server 2008 und Windows Vista hinzugefügt. Ein Standardbenutzerkonto ist synonym mit einem Benutzerkonto in Windows XP. Benutzerkonten, die Mitglieder der lokalen Administratorgruppe sind, führen die meisten Anwendungen als Standardbenutzer aus.

Informationen zur UAC finden Sie in den folgenden Themen.



| Thema                                                                                                                                        | BESCHREIBUNG                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Richtlinien für die Benutzerkontensteuerung in der Benutzeroberflächenentwicklung](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)<br/> | Allgemeine Informationen zur UAC.<br/>                                                                                                     |
| [Entwickeln von Anwendungen, die Administratorrechte erfordern](developing-applications-that-require-administrator-privilege.md)<br/>  | Modelle für die Entwicklung von Anwendungen, die Vorgänge ausführen, die Administratorrechte erfordern, aber als Standardbenutzer ausgeführt werden.<br/> |
| [Autorisierungsreferenz](authorization-reference.md)<br/>                                                                            | Ausführliche Informationen zu Autorisierungsfunktionen, Schnittstellen, Strukturen und anderen Programmierelementen.<br/>                        |



 

 

 




