---
description: In diesem Thema wird erläutert, wie neue Dateitypen erstellt werden und wie Sie Ihre APP mit dem Dateityp und anderen klar definierten Dateitypen verknüpfen.
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: Dateitypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d697c42626c6e1ab3e0b5cc0b88bd065523d53a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979744"
---
# <a name="file-types"></a>Dateitypen

In diesem Thema wird erläutert, wie neue Dateitypen erstellt werden und wie Sie Ihre APP mit dem Dateityp und anderen klar definierten Dateitypen verknüpfen. Dateien mit einer gemeinsamen Dateinamenerweiterung (doc, HTML usw.) weisen denselben *Typ* auf. Wenn Sie z. b. einen neuen Text-Editor erstellen, können Sie den vorhandenen txt-Dateityp verwenden. In anderen Fällen müssen Sie möglicherweise einen neuen Dateityp erstellen.

Dieses Thema ist wie folgt organisiert:

-   [Öffentliche und private Dateitypen](#public-and-private-file-types)
-   [Registrieren eines Dateityps](#registering-a-file-type)
    -   [Festlegen optionaler Unterschlüssel und Dateityp Erweiterungs Attribute](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [Löschen von Registrierungsinformationen während der deinstalstallation](#deleting-registry-information-during-uninstallation)
-   [Dateitypen, die offene Metadaten unterstützen](#file-types-that-support-open-metadata)
-   [Zugehörige Themen](#related-topics)

Weitere Informationen finden Sie in den folgenden Themen:

-   [Vorgehensweise beim Auswählen einer Dateityp Erweiterung](how-to-choose-a-file-type-extension.md)
-   [Definieren von Dateityp Attributen](./how-to-define-file-type-attributes.md)
-   [Einschließen einer Anwendung im Dialog Feld "Öffnen mit"](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [Ausschließen einer Anwendung aus dem Dialog Feld "Öffnen mit" für nicht zugeordnete Dateitypen](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a>Öffentliche und private Dateitypen

Öffentliche Dateitypen werden auch als beliebte oder strittige Typen bezeichnet, da konkurrierende Anwendungen diesen Dateitypen zugeordnet werden können. Zu den Merkmalen der öffentlichen Dateitypen gehören:

-   Sie werden in der Regel in Standard Textteilen definiert und/oder werden von ihren definierenden Organisationen als Austauschformate herauf gestuft.
-   Sie werden häufig für verschiedene Zwecke zwischen Computern und Benutzern ausgetauscht.
-   Sie müssen auf vielen verschiedenen Plattformen unterstützt werden.
-   Anwendungen von mehreren Anbietern werden diese wahrscheinlich verarbeiten.

Einige Beispiele für Dateitypen, die als öffentlich angesehen werden, sind die Bild Dateitypen PNG, GIF, JPG und BMP sowie die Audiotypen. wav,. MP3 und. au.

Im Gegensatz zu öffentlichen Dateitypen verfügen private oder proprietäre Dateitypen in der Regel über ein Format, das nur von einer Anwendung oder einem Anbieter implementiert und verstanden wird. Folglich sind private Dateitypen in der Regel nicht anfällig für Konflikte zwischen Anwendungen. Einige Dateitypen können als private Dateitypen gestartet werden, werden jedoch später zu öffentlichen Dateitypen.

> [!Note]  
> Windows unterscheidet nicht zwischen öffentlichen und privaten Dateitypen. Der Unterschied ist nur wichtig, um Entscheidungen über die Wahl der Dateityp Registrierung zu treffen.

 

## <a name="registering-a-file-type"></a>Registrieren eines Dateityps

Um den Dateityp einer vorhandenen Anwendung zuzuordnen, suchen Sie die Anwendungs ProgID in der Registrierung. Um den Dateityp einer neuen Anwendung zuzuordnen, definieren Sie eine ProgID für Ihre Anwendung. Weitere Informationen zum Definieren einer neuen ProgID [finden Sie](fa-progids.md)Unterprogramm gesteuerte Bezeichner.

Die Unterschlüssel der Dateinamenerweiterung weisen die folgende allgemeine Form auf: *Erweiterung* = *ProgID*. Die Unterschlüssel der Dateinamenerweiterung werden in der Stamm Struktur der **HKEY- \_ Klassen \_** gespeichert.

Beim Erstellen von Dateityp unter Schlüsseln in der Registrierung ist es wichtig, den führenden Zeitraum (.) einzubeziehen. Wenn Sie z. b. möchten, dass ein Dateityp mit der kurzen Erweiterung. MYP und der Long-Erweiterung. MYP-File mit einer Anwendung namens myprogram geöffnet wird, verwenden Sie die folgende Syntax:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

Wie im vorherigen Beispiel gezeigt, sollten Sie, wenn Sie auch eine kurze Dateinamenerweiterung (. MYP) registrieren, einen Unterschlüssel für die Long-Erweiterung (MYP-Datei) erstellen. Weitere Informationen finden Sie unter [Dateityp Handler](fa-file-extensions.md).

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a>Festlegen optionaler Unterschlüssel und Dateityp Erweiterungs Attribute

Dateityp-Erweiterungs Einträge in der Registrierung verfügen über mehrere optionale Unterschlüssel und Attribute.

Die von Dateizuordnungen verwendeten Dateityp-Erweiterungs Einträge werden in der folgenden Tabelle beschrieben. Alle Werte sind vom Typ " **reg \_ SZ** ".



| Registrierungseintrag  | Action                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Standard         | Legen Sie den Standardwert des Erweiterungs unter Schlüssels auf die ProgID fest, mit der er verknüpft ist.                                                                                                                                                                                                                                                 |
| Inhaltstyp    | Legen Sie den Wert Inhaltstyp auf den MIME-Inhaltstyp des Dateityps fest.                                                                                                                                                                                                                                                                   |
| OpenWithList    | Darf nicht verwendet werden. Dieser Unterschlüssel enthält mindestens einen Anwendungs Unterschlüssel für Anwendungen, die im Dialogfeld **Öffnen mit** für den Dateityp angezeigt werden, und ist nur für exe-Anwendungen auf Betriebssystemen vor Windows XP vorgesehen. Verwenden Sie stattdessen OpenWithProgIds.                                                            |
| OpenWithProgIds | Dieser Unterschlüssel enthält eine Liste alternativer ProgIDs für diesen Dateityp. Die Programme für diese ProgIDs werden im Menü **Öffnen mit** angezeigt und sind als Standard-Windows Store-Apps für den Dateityp verfügbar. Wenn eine Anwendung diesen Dateityp durch Ändern des Standardwerts übernimmt, sollte dieser Liste auch ein Eintrag hinzugefügt werden. |
| Wahrnehmungstyp   | Legen Sie den Wert von "wahrnehmvedtype" auf den "wahrnehmvedtype" fest, zu dem die Datei gehört, falls vorhanden. Diese Zeichenfolge wird von Windows-Versionen vor Windows Vista nicht verwendet. Weitere Informationen finden Sie unter [wahrgenommene Typen und Anwendungs Registrierung](fa-perceivedtypes.md).                                                                           |



 

Die allgemeine Form des unter Schlüssels für die Dateinamenerweiterung lautet wie folgt. Alle Eintrags Typen haben den Typ " **reg \_ SZ** ".

```
HKEY_CLASSES_ROOT
   .ext
      (Default) = ProgID.ext.1
      Content Type = MIME content type
      PerceivedType = PerceivedType
      OpenWithProgids
         ProgID2.ext.1
         ProgID3.ext.1
      ProgID.ext.1
         shellnew
```

Wichtige Überlegungen zu Dateitypen:

-   Die Stamm Unterstruktur der **HKEY- \_ Klassen \_** ist eine Ansicht, die durch Zusammenführen von **aktuellen HKEY- \_ \_ Benutzer** \\ **Software** \\ **Klassen** und **HKEY- \_ \_** \\ **Software** \\ **Klassen** für lokale Computer
-   Im Allgemeinen ist der Stamm der **HKEY- \_ Klassen \_** das Lesen aus, aber nicht das Schreiben in. Weitere Informationen finden Sie im Stamm Artikel [HKEY \_ Classes \_ ](../sysinfo/hkey-classes-root-key.md) .
-   Um einen Dateityp Global auf einem bestimmten Computer zu registrieren, erstellen Sie einen Eintrag für den Dateityp im Unterschlüssel **HKEY \_ local \_ Machine** \\  \\ **Classes Software Classes** .
-   Wenn Sie eine Dateityp Registrierung nur für den aktuellen Benutzer sichtbar machen möchten, erstellen Sie im Unterschlüssel **HKEY \_ Current \_ User** \\ **Software** \\ **Classes** einen Eintrag für den Dateityp.
-   Eine Anwendung kann eine eigene Implementierung eines Verbs bereitstellen, wie z. b. "Open" oder "Play", wie im folgenden Registrierungs Beispiel dargestellt.

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    Zu den unter Schlüsseln des Verb-unter Schlüssels gehören die Befehlszeile und die Drop Target-Methode: **Command** und **DropTarget**.

-   Wenn Sie eine Datei Zuordnung erstellen oder ändern, ist es wichtig, das System zu benachrichtigen, dass Sie eine Änderung vorgenommen haben. Rufen Sie hierzu " [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) " auf, und geben Sie das **shcne-Ereignis " \_ assocchanged** " an. Wenn Sie **shchangenotify** nicht aufrufen, wird die Änderung möglicherweise erst erkannt, nachdem das System neu gestartet wurde.
-   Zum Abrufen von Registrierungsinformationen bezüglich einer Datei Zuordnung verwenden Sie die [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Schnittstelle. Ein Szenario, in dem diese Vorgehensweise veranschaulicht wird, finden Sie unter [Beispielszenario für Datei](fa-sample-scenarios.md)Zuordnung.

> [!Note]  
> Die Registrierungs Unterschlüssel **App-Pfade** und **Anwendungen** werden verwendet, um das Verhalten des Systems im Auftrag von Anwendungen zu registrieren und zu steuern. Ausführlichere Informationen zu dieser Funktion finden Sie unter [Anwendungs Registrierung](app-registration.md).

 

### <a name="deleting-registry-information-during-uninstallation"></a>Löschen von Registrierungsinformationen während der deinstalstallation

Beim Deinstallieren einer Anwendung sollten die ProgIDs und die meisten anderen Registrierungsinformationen, die dieser Anwendung zugeordnet sind, im Rahmen der deinstallieren gelöscht werden. Anwendungen, die den Besitz eines Dateityps übernommen haben (indem Sie den Standardwert der **HKEY- \_ Klassen " \_ root**. Extension" des Dateityps \\  für die ProgID der Anwendung festlegen), sollten diesen Wert beim Deinstallieren nicht entfernen. Wenn die Daten für den Standardwert nicht vorhanden sind, wird vermieden, dass Sie feststellen, ob eine andere Anwendung den Besitz des Dateityps übernommen hat, und den Standardwert überschrieben haben, nachdem die ursprüngliche Anwendung installiert wurde. Windows respektiert den Standardwert nur dann, wenn die ProgID gefunden wurde, die eine registrierte ProgID enthält. Wenn die Registrierung der ProgID aufgehoben wird, wird Sie ignoriert.

Beachten Sie, dass weitere Besitz Informationen für den Dateityp in der **aktuellen HKEY- \_ \_ Benutzer** Unterstruktur gespeichert werden und nur dann verwendet werden, wenn die Anwendung, auf die verwiesen wird, registriert ist. Daher müssen diese Daten beim Deinstallieren einer Anwendung nicht entfernt werden.

Im folgenden Beispiel wird der Status der Registrierung angezeigt, bevor eine Anwendung deinstalliert wird:

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID
      shell
         open
            command
               (Default) = yourapp.exe %1
```

Im folgenden wird der Zustand der gleichen Registrierungseinträge nach der Installation der Anwendung angezeigt.

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a>Dateitypen, die offene Metadaten unterstützen

In Windows 7 und höher unterstützen die folgenden Dateitypen geöffnete Metadaten.



| Dateityp                                                               | Dateinamen Erweiterungen                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| Office 2007-Dokumente                                                   | . docx,. xlsx,. pptx                                           |
| Office 97-2003-Dokumente                                                | . doc,. xls,. ppt                                              |
| Gespeicherte Suche                                                            | . Search-MS                                                    |
| Windows Media-basierte Formate (Advanced Streaming Format (ASF)-Container) | WMV,. WMA                                                    |
| MP4 (Eigenschaften Handler)                                                  | . MP4,. m4a,. m4v,. MP4V,. m4p,. M4B,. 3GP,. 3GPP,. 3gp2,. mov |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Registrierung](app-registration.md)
</dt> <dt>

[Funktionsweise von Dateizuordnungen](fa-how-work.md)
</dt> <dt>

[Inhaltsansicht nach Dateityp oder-Art](prophand-content-view.md)
</dt> <dt>

[Dateityp Überprüfung](file-type-verifier.md)
</dt> <dt>

[Dateityp Handler](fa-file-extensions.md)
</dt> <dt>

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> <dt>

[Zuordnungs Arrays](fa-associationarray.md)
</dt> </dl>

 

 
