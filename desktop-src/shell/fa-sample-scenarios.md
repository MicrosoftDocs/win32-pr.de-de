---
description: Im folgenden Beispiel wird ein hypothetisches Softwareentwicklungsunternehmen namens Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Beispiel für Datei Zuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4104c9bc241fed4bc698bd150b03d32a70e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127868"
---
# <a name="file-association-example"></a>Beispiel für Datei Zuordnung

Im folgenden Beispiel erstellt ein hypothetisches Softwareentwicklungsunternehmen namens Litware, Inc. einen neuen Audioplayer namens litwareplayer. Litware möchte eine Datei Zuordnung zwischen litwareplayer und dessen primärem Dateityp entwerfen, der ein neu entwickeltes Audioformat verwendet, das eine gesamte AudioCD in weniger als 10 Kilobyte Arbeitsspeicher ohne Qualitätsverlust speichern kann.

> [!IMPORTANT]
> Dieses Thema gilt nicht für Windows 10. Die Art und Weise, wie standardmäßige Dateizuordnungen in Windows 10 geändert werden. Weitere Informationen finden Sie im Abschnitt zu den **Änderungen in Windows 10** für die Behandlung von Standard-apps in [diesem Beitrag](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

## <a name="designing-a-new-file-association"></a>Entwerfen einer neuen Datei Zuordnung

Das Unternehmen sollte die folgenden Schritte ausführen.

1.  **Entscheiden Sie, ob der neue Dateityp als öffentlich oder privat behandelt werden soll.** Dieser neue Dateityp ist ein Medientyp. Da Benutzer Mediendateien auf verschiedenen Plattformen austauschen und es möglicherweise andere Anwendungen gibt, die das litwareplayer-Format lesen müssen, ist ein [öffentlicher](fa-file-types.md) Dateityp die geeignetste.
2.  **Bestimmen Sie, ob dieser Dateityp bereits definiert ist.** Überprüfen Sie die Internet Assigned Numbers Authority (IANA)-MIME-Datenbank und andere öffentliche Dateityp Datenbanken im Internet, um zu bestimmen, dass kein vergleichbarer Dateityp definiert wurde. Da es sich um ein neues Dateiformat handelt, müssen Sie einen neuen Dateityp definieren.
3.  **Definieren Sie eine Dateinamenerweiterung für den neuen Dateityp.** Die Entwickler wählen den aus `.opa-ltw-audio` , der seine Hersteller Abkürzung und einen Hinweis zum Inhalt der Datei enthält. Research stellt fest, dass die Erweiterung nicht von anderen Personen verwendet wird. Im Anschluss an die aktuellen Empfehlungen ist keine kurze Erweiterung definiert.
4.  **Definieren Sie einen MIME-Typ für den Dateityp, und registrieren Sie ihn bei der IANA.** Litware definiert den neuen MIME-Typ als *Audiodatei/litwareplayer. 1* und bereitet eine MIME-Typanwendung vor, indem er die in Request for Comments (RFC)-Nummern 2045, 2046, 2047 und 2048 aufgeführten Richtlinien unter folgt. Anschließend übermitteln Sie die Anwendung an die IANA, mit der der neue Dateityp der Datenbank registrierter MIME-Typen hinzugefügt wird.
5.  **Stellen Sie fest, ob eine ProgID für den Dateityp vorhanden ist.** Da es sich um einen neuen Dateityp handelt, ist keine [ProgID](fa-progids.md) vorhanden. Litware legt fest, wie eine neue ProgID für litwareplayer entworfen wird. Sie entscheiden sich für den anzeigen Amen "litwareplayer-Audioplayer" (der als Ressource in der LitwarePlayer.exe-Datei gespeichert ist) und entwerfen ein Standard Symbol für Dateien, die mit litwareplayer verknüpft sind (ebenfalls in LitwarePlayer.exe gespeichert). Da litwareplayer eine neue Anwendung ist, ist dies eine ProgID der Version 1.
6.  **Registrieren Sie die ProgID.** Wenn litwareplayer installiert ist, erstellt das Installationsprogramm den folgenden [ProgID](fa-progids.md) -Eintrag in der Registrierung.

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

    In der Befehlstaste wird %1 als Pfad zur wieder zugebende Datei übermittelt.

7.  **Registrieren Sie die Dateinamenerweiterung für den Dateityp.** Wenn litwareplayer installiert ist, erstellt das Installationsprogramm die folgenden Einträge für die benutzerdefinierte Dateityp Erweiterung in der Registrierung.

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> Wenn eine Datei Zuordnung erstellt oder geändert wird, Benachrichtigen Sie das System, dass durch Aufrufen von [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)eine Änderung vorgenommen wurde, und geben Sie dabei das shcne- \_ Ereignis "assocchanged" an. Wenn dies nicht der Fall ist, erkennt die Shell möglicherweise keine Änderungen, die bis zum Systemneustart vorgenommen wurden.

 

## <a name="additional-resources"></a>Weitere Ressourcen

-   [Einführung in Dateizuordnungen](fa-intro.md)
-   [Registrieren eines Internet Browsers oder e-Mail-Clients über das Windows-Startmenü](start-menu-reg.md)
-   [Registrieren einer Anwendung in einem URI-Schema](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bewährte Methoden für Dateizuordnungen](fa-best-practices.md)
</dt> <dt>

[Richtlinien für die Verwaltung von Standardanwendungen in Windows Vista und höher](vista-managing-defaults.md)
</dt> <dt>

[Standardprogramme](default-programs.md)
</dt> <dt>

[Festlegen des Programm Zugriffs und der Computer Standardwerte (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
