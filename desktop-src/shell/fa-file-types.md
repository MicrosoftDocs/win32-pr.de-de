---
description: In diesem Thema wird erläutert, wie Sie neue Dateitypen erstellen und Ihre App Ihrem Dateityp und anderen klar definierten Dateitypen zuordnen.
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: Dateitypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 541e6068237b504ea8c9faf06e2083986ed5bb48a7c16dabb82e5096569d9f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094205"
---
# <a name="file-types"></a>Dateitypen

In diesem Thema wird erläutert, wie Sie neue Dateitypen erstellen und Ihre App Ihrem Dateityp und anderen klar definierten Dateitypen zuordnen. Dateien mit einer gemeinsamen Dateinamenerweiterung (.doc, .html usw.) haben denselben *Typ.* Wenn Sie z. B. einen neuen Text-Editor erstellen, können Sie den vorhandenen .txt Dateityp verwenden. In anderen Fällen müssen Sie möglicherweise einen neuen Dateityp erstellen.

Dieses Thema ist wie folgt organisiert:

-   [Öffentliche und private Dateitypen](#public-and-private-file-types)
-   [Registrieren eines Dateityps](#registering-a-file-type)
    -   [Festlegen optionaler Unterschlüssel und Dateierweiterungsattribute](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [Löschen von Registrierungsinformationen während der Deinstallation](#deleting-registry-information-during-uninstallation)
-   [Dateitypen, die geöffnete Metadaten unterstützen](#file-types-that-support-open-metadata)
-   [Zugehörige Themen](#related-topics)

Weitere Informationen finden Sie in den folgenden Themen:

-   [Auswählen einer Dateierweiterung](how-to-choose-a-file-type-extension.md)
-   [Definieren von Dateitypattributen](./how-to-define-file-type-attributes.md)
-   [Einschließen einer Anwendung in das Dialogfeld "Öffnen mit"](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [Ausschließen einer Anwendung aus dem dialogfeld "Öffnen mit" für nicht zugeordnete Dateitypen](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a>Öffentliche und private Dateitypen

Öffentliche Dateitypen werden auch als beliebte oder umständliche Typen bezeichnet, da konkurrierende Anwendungen diesen Dateitypen möglicherweise zugeordnet werden möchten. Zu den Merkmalen öffentlicher Dateitypen gehören:

-   Sie werden in der Regel durch Standardkörper definiert und/oder von ihren definierenden Organisationen als Austauschformate heraufgestuft.
-   Sie werden häufig für verschiedene Zwecke zwischen Computern und Benutzern ausgetauscht.
-   Sie müssen auf vielen verschiedenen Plattformen unterstützt werden.
-   Anwendungen von mehreren Anbietern werden diese wahrscheinlich verarbeiten.

Einige Beispiele für Dateitypen, die als öffentlich betrachtet werden, sind die Bilddateitypen .png, .gif, .jpg und .bmp sowie die Audiotypen WAV, .mp3 und AU.

Im Gegensatz zu öffentlichen Dateitypen weisen private oder proprietäre Dateitypen in der Regel ein Format auf, das nur von einer Anwendung oder einem Anbieter implementiert und verstanden wird. Daher sind private Dateitypen in der Regel nicht anfällig für Konflikte zwischen Anwendungen. Einige Dateitypen können als private Dateitypen beginnen, aber später zu öffentlichen Dateitypen werden.

> [!Note]  
> Windows unterscheidet nicht zwischen öffentlichen und privaten Dateitypen. Die Unterscheidung ist nur relevant, wenn Sie Entscheidungen zur Wahl der Dateitypregistrierung treffen.

 

## <a name="registering-a-file-type"></a>Registrieren eines Dateityps

Um den Dateityp einer vorhandenen Anwendung zuzuordnen, suchen Sie die ProgID der Anwendung in der Registrierung. Um den Dateityp einer neuen Anwendung zuzuordnen, definieren Sie eine ProgID für Ihre Anwendung. Informationen zum Definieren einer neuen ProgID finden Sie unter [Programmgesteuerte Bezeichner.](fa-progids.md)

Unterschlüssel für Dateinamenerweiterungen weisen die folgende allgemeine Form auf: = *Erweiterung ProgID*. Unterschlüssel der Dateinamenerweiterung werden in der **\_ \_ Stammstruktur HKEY CLASSES** gespeichert.

Es ist wichtig, den führenden Punkt (.) beim Erstellen von Dateitypunterschlüsseln in die Registrierung einzubeziehen. Wenn Sie beispielsweise einen Dateityp mit der kurzen Erweiterung .myp und der langen Erweiterung .myp-file mit einer Anwendung namens MyProgram öffnen möchten, verwenden Sie die folgende Syntax:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

Wie im vorherigen Beispiel gezeigt, sollten Sie auch einen Unterschlüssel für die lange Erweiterung (.myp-file) erstellen, wenn Sie auch eine kurze Dateinamenerweiterung (.myp) registrieren. Weitere Informationen finden Sie unter [Dateityphandler.](fa-file-extensions.md)

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a>Festlegen optionaler Unterschlüssel und Dateierweiterungsattribute

Dateityperweiterungseinträge in der Registrierung verfügen über mehrere optionale Unterschlüssel und Attribute.

Die Von Dateizuordnungen verwendeten Dateityperweiterungseinträge werden in der folgenden Tabelle beschrieben. Alle Werte haben den **REG \_ SZ-Typ.**



| Registrierungseintrag  | Aktion                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Standard         | Legen Sie den Standardwert des Erweiterungsunterschlüssels auf die ProgID fest, mit der er verknüpft ist.                                                                                                                                                                                                                                                 |
| Inhaltstyp    | Legen Sie den Wert für Inhaltstyp auf den MIME-Inhaltstyp des Dateityps fest.                                                                                                                                                                                                                                                                   |
| OpenWithList    | Darf nicht verwendet werden. Dieser Unterschlüssel enthält einen oder mehrere Anwendungsunterschlüssel für Anwendungen, die im Dialogfeldeintrag **Öffnen mit** für den Dateityp angezeigt werden und nur für .exe Anwendungen unter Betriebssystemen vor Windows XP vorgesehen sind. Verwenden Sie stattdessen OpenWithProgIds.                                                            |
| OpenWithProgIds | Dieser Unterschlüssel enthält eine Liste alternativer ProgIDs für diesen Dateityp. Die Programme für diese ProgIDs werden im **menü Öffnen mit** angezeigt und sind standardmäßig Windows Store Apps für den Dateityp verfügbar. Wenn eine Anwendung diesen Dateityp übernimmt, indem sie den Standardwert ändert, sollte sie dieser Liste auch einen Eintrag hinzufügen. |
| PerceivedType   | Legen Sie den Wert für PerceivedType auf den PerceivedType fest, zu dem die Datei gehört( falls vorhanden). Diese Zeichenfolge wird von Windows Versionen vor Windows Vista nicht verwendet. Weitere Informationen finden Sie unter [Wahrgenommene Typen und Anwendungsregistrierung.](fa-perceivedtypes.md)                                                                           |



 

Die allgemeine Form eines Unterschlüssels für die Dateinamenerweiterung lautet wie folgt. Alle Eintragstypen haben den **REG \_ SZ-Typ.**

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

Wichtige Überlegungen zu Dateitypen sind:

-   Die **Stammstruktur HKEY \_ CLASSES \_** ist eine Sicht, die durch Zusammenführen von **HKEY CURRENT \_ \_ USER** \\ **Software** \\ **Classes** und **HKEY LOCAL \_ \_ MACHINE** \\ **Software** \\ **Classes** gebildet wird.
-   Im Allgemeinen soll **HKEY \_ CLASSES \_ ROOT** aus gelesen, aber nicht in geschrieben werden. Weitere Informationen finden Sie im Artikel [HKEY \_ CLASSES \_ ROOT.](../sysinfo/hkey-classes-root-key.md)
-   Um einen Dateityp global auf einem bestimmten Computer zu registrieren, erstellen Sie im Unterschlüssel **HKEY \_ LOCAL \_ MACHINE** Software Classes einen Eintrag für den \\  \\  Dateityp.
-   Um eine Dateitypregistrierung nur für den aktuellen Benutzer sichtbar zu machen, erstellen Sie im Unterschlüssel **HKEY \_ CURRENT \_ USER** Software Classes einen Eintrag für den \\  \\  Dateityp.
-   Eine Anwendung kann eine eigene Implementierung eines Verbs bereitstellen, z. B. "open" oder "play", wie im folgenden Registrierungsbeispiel gezeigt.

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    Unterschlüssel des Verbunterschlüssels enthalten die Befehlszeile und die Drop-Zielmethode: **command** und **DropTarget**.

-   Wenn Sie eine Dateizuordnung erstellen oder ändern, ist es wichtig, das System zu benachrichtigen, dass Sie eine Änderung vorgenommen haben. Rufen Sie dazu [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) auf, und geben Sie das **SHCNE \_ ASSOCCHANGED-Ereignis** an. Wenn Sie **SHChangeNotify** nicht aufrufen, wird die Änderung möglicherweise erst nach dem Neustart des Systems erkannt.
-   Verwenden Sie die [**IQueryAssociations-Schnittstelle,**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) um Registrierungsinformationen zu einer Dateizuordnung abzurufen. Ein Szenario, das dieses Verfahren veranschaulicht, finden Sie unter Beispielszenario für [die Dateizuordnung.](fa-sample-scenarios.md)

> [!Note]  
> Sowohl die Unterschlüssel **App-Pfade** als auch **Anwendungsregistrierung** werden verwendet, um das Verhalten des Systems im Auftrag von Anwendungen zu registrieren und zu steuern. Ausführlichere Informationen zu dieser Funktion finden Sie unter [Anwendungsregistrierung.](app-registration.md)

 

### <a name="deleting-registry-information-during-uninstallation"></a>Löschen von Registrierungsinformationen während der Deinstallation

Beim Deinstallieren einer Anwendung sollten die ProgIDs und die meisten anderen Registrierungsinformationen, die dieser Anwendung zugeordnet sind, im Rahmen der Deinstallation gelöscht werden. Anwendungen, die den Besitz eines Dateityps übernommen haben (durch Festlegen des Standardwerts des **Unterschlüssels HKEY \_ CLASSES \_ ROOT**.extension des Dateityps \\  auf die ProgID der Anwendung), sollten bei der Deinstallation jedoch nicht versuchen, diesen Wert zu entfernen. Wenn Sie die Daten für den Standardwert belassen, müssen Sie nicht feststellen, ob eine andere Anwendung den Besitz des Dateityps übernommen und den Standardwert nach der Installation der ursprünglichen Anwendung überschrieben hat. Windows wird der Standardwert nur dann beachtet, wenn die ProgID eine registrierte ProgID gefunden hat. Wenn die Registrierung der ProgID aufgehoben wird, wird sie ignoriert.

Beachten Sie, dass andere Dateitypbesitzinformationen in der **HKEY \_ CURRENT \_ USER-Unterstruktur** gespeichert werden und nur verwendet werden, wenn die Anwendung registriert ist, auf die sie verweist. Daher müssen diese Daten beim Deinstallieren einer Anwendung nicht entfernt werden.

Das folgende Beispiel zeigt den Status der Registrierung, bevor eine Anwendung deinstalliert wird:

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

Im Folgenden wird der Status derselben Registrierungseinträge nach der Deinstallation der Anwendung angezeigt.

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a>Dateitypen, die geöffnete Metadaten unterstützen

In Windows 7 und höher unterstützen die folgenden Dateitypen geöffnete Metadaten.



| Dateityp                                                               | Dateinamenerweiterungen                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| Office 2007-Dokumente                                                   | .docx, .xlsx, .pptx                                           |
| dokumente Office 97-2003                                                | .doc, .xls, .ppt                                              |
| Gespeicherte Suche                                                            | .search-ms                                                    |
| Windows Medienbasierte Formate (ASF-Container (Advanced Streaming Format) | .wmv, .wma                                                    |
| MP4 (Eigenschaftenhandler)                                                  | .mp4, .m4a, .m4v, .mp4v, .m4p, .m4b, .3gp, .3gpp, .3gp2, .mov |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsregistrierung](app-registration.md)
</dt> <dt>

[Funktionsweise von Dateizuordnungen](fa-how-work.md)
</dt> <dt>

[Inhaltsansicht nach Dateityp oder Art](prophand-content-view.md)
</dt> <dt>

[Dateitypüberprüfung](file-type-verifier.md)
</dt> <dt>

[Dateityphandler](fa-file-extensions.md)
</dt> <dt>

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> <dt>

[Zuordnungsarrays](fa-associationarray.md)
</dt> </dl>

 

 
