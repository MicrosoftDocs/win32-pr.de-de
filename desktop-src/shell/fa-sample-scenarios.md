---
description: Im folgenden Beispiel ist dies ein hypothetisches Softwareentwicklungsunternehmen namens Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Dateiassozbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad24c3e65ca5b297412c4a69702987cd86b5187dab63dd81435d50e7d06721d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009530"
---
# <a name="file-association-example"></a>Dateiassozbeispiel

Im folgenden Beispiel erstellt ein hypothetisches Softwareentwicklungsunternehmen namens Litware, Inc. einen neuen Audioplayer namens LitwarePlayer. Litware möchte eine Dateiassozierung zwischen LitwarePlayer und seinem primären Dateityp entwerfen. Dabei wird ein neu entwickeltes Audioformat verwendet, das es ermöglicht, eine gesamte Audio-CD in weniger als 10 KB Arbeitsspeicher ohne Qualitätsverlust zu speichern.

> [!IMPORTANT]
> Dieses Thema gilt nicht für Windows 10. Die Art und Weise, wie Standarddateizuordnungen funktionieren, hat sich in Windows 10. Weitere Informationen finden Sie im Abschnitt Änderungen an der Art und Weise, wie Windows 10 **Standard-Apps** behandelt, in [diesem Beitrag.](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)

 

## <a name="designing-a-new-file-association"></a>Entwerfen einer neuen Dateiassozierung

Das Unternehmen sollte die folgenden Schritte ausführen.

1.  **Entscheiden Sie, ob der neue Dateityp als öffentlich oder privat behandelt werden soll.** Dieser neue Dateityp ist ein Medientyp. Da Benutzer Mediendateien plattformübergreifend austauschen und es möglicherweise andere Anwendungen gibt, [](fa-file-types.md) die das LitwarePlayer-Format lesen müssen, ist ein öffentlicher Dateityp am besten geeignet.
2.  **Bestimmen Sie, ob dieser Dateityp bereits definiert ist.** Überprüfen Sie die MIME-Datenbank (Internet Assigned Numbers Authority, IANA) und andere öffentliche Dateitypdatenbanken im Internet, um festzustellen, ob kein vergleichbarer Dateityp definiert wurde. Da es sich um ein neues Dateiformat handelt, müssen Sie einen neuen Dateityp definieren.
3.  **Definieren Sie eine Dateierweiterung für den neuen Dateityp.** Die Entwickler wählen die aus, die ihre Herstellerabkürzung und einen Hinweis dazu enthält, `.opa-ltw-audio` was die Datei enthält. Untersuchungen legen fest, dass die Erweiterung nicht von anderen Personen verwendet wird. Gemäß den aktuellen Empfehlungen ist keine kurze Erweiterung definiert.
4.  **Definieren Sie einen MIME-Typ für den Dateityp, und registrieren Sie ihn bei der IANA.** Litware definiert den neuen MIME-Typ als *audio/LitwarePlayer.1* und bereitet eine MIME-Typanwendung gemäß den Richtlinien unter RFC-Nummern 2045, 2046, 2047 und 2048 vor. Anschließend übermitteln sie die Anwendung an die IANA, die der Datenbank mit registrierten MIME-Typen den neuen Dateityp hinzufügt.
5.  **Bestimmen Sie, ob eine ProgID für den Dateityp vorhanden ist.** Da es sich um einen neuen Dateityp handelt, ist dafür [keine ProgID](fa-progids.md) vorhanden. Litware setzt auf das Entwerfen einer neuen ProgID für LitwarePlayer. Sie entscheiden sich für den Benutzerfreundlichen Namen "LitwarePlayer Audio Player" (der als Ressource in der LitwarePlayer.exe-Datei gespeichert ist) und entwerfen ein Standardsymbol für Dateien, die LitwarePlayer zugeordnet sind (auch in LitwarePlayer.exe). Da LitwarePlayer eine neue Anwendung ist, ist dies eine ProgID der Version 1.
6.  **Registrieren Sie die ProgID.** Wenn LitwarePlayer installiert ist, erstellt das Installationsprogramm den folgenden [ProgID-Eintrag](fa-progids.md) in der Registrierung.

    ```
    HKEY_CLASSES_ROOT
       Litware.LitwarePlayer.1
          (Default) = LitwarePlayer Audio Player
          FriendlyTypeName = @LitwarePlayer, -120
          CurVer
             (Default) = Litware.LitwarePlayer.1
          DefaultIcon
             (Default) = LitwarePlayer, -142
          shell
             play
                command
                   (Default) = "%ProgramFiles%\LitwarePlayer\LitwarePlayer.exe" "%1"
    ```

    Im Befehlsschlüssel wird %1 als Pfad zur datei übergeben, die wieder verwendet werden soll.

7.  **Registrieren Sie die Dateierweiterung für den Dateityp.** Wenn LitwarePlayer installiert ist, erstellt das Installationsprogramm die folgenden Einträge in der Registrierung für die benutzerdefinierte Dateityperweiterung.

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> Wenn eine Dateiassozierung erstellt oder geändert wird, benachrichtigen Sie das System, dass eine Änderung vorgenommen wurde, indem Sie [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)aufrufen und das SHCNE \_ ASSOCCHANGED-Ereignis angeben. Wenn dies nicht erfolgt, erkennt die Shell möglicherweise keine Änderungen, die vorgenommen wurden, bevor das System neu gestartet wird.

 

## <a name="additional-resources"></a>Weitere Ressourcen

-   [Einführung in Dateizuordnungen](fa-intro.md)
-   [Registrieren eines Internetbrowsers oder E-Mail-Clients über Windows Startmenü](start-menu-reg.md)
-   [Registrieren einer Anwendung für ein URI-Schema](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bewährte Methoden für Dateizuordnungen](fa-best-practices.md)
</dt> <dt>

[Richtlinien für die Verwaltung von Standardanwendungen in Windows Vista und höher](vista-managing-defaults.md)
</dt> <dt>

[Standardprogramme](default-programs.md)
</dt> <dt>

[Festlegen von Programmzugriff und Computereinstellungen (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
