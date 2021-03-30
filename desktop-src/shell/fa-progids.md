---
description: Die Shell verwendet einen ProgID-Registrierungs Unterschlüssel (programmgesteuerte Bezeichner), um einer Anwendung einen Dateityp zuzuordnen und das Verhalten der Zuordnung zu steuern.
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: Programmgesteuerte Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67720fed1ad4b8401d11f6532cdc79836911e7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993710"
---
# <a name="programmatic-identifiers"></a>Programmgesteuerte Bezeichner

Die Shell verwendet einen ProgID-Registrierungs Unterschlüssel (programmgesteuerte Bezeichner), um einer Anwendung einen Dateityp zuzuordnen und das Verhalten der Zuordnung zu steuern. Die für Dateizuordnungen verwendeten ProgID-Einträge befinden sich in der Registrierung unter **HKEY \_ Classes \_ root** .

Dieses Thema ist wie folgt organisiert:

-   [Von Dateizuordnungen verwendete programmatische bezeichnerelemente](#programmatic-identifier-elements-used-by-file-associations)
-   [Verwenden von programmatischen bezeichlern mit Versions Angabe](#using-versioned-programmatic-identifiers)
-   [Zugehörige Themen](#related-topics)

Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren eines Dateityps für eine neue Anwendung](how-to-register-a-file-type-for-a-new-application.md) .

## <a name="programmatic-identifier-elements-used-by-file-associations"></a>Von Dateizuordnungen verwendete programmatische bezeichnerelemente

Das richtige Format eines ProgID-Schlüssel namens ist " \[ *Vendor" oder "Application*" \] . \[ *Komponente* \] . \[ *Version* \] , getrennt durch Punkte und ohne Leerzeichen, wie in Word.Doc-Nummer. 6. Der *Versions* Anteil ist optional, wird jedoch dringend empfohlen. Weitere Informationen finden Sie unter [Verwenden von programmatischen bezeichlern mit Versions](#using-versioned-programmatic-identifiers)Angabe.

Ein ProgID-Unterschlüssel sollte die folgenden Elemente enthalten. Beachten Sie, dass für einige Zeichen folgen Daten in diesem Schlüssel eine bestimmte Formatierung erforderlich ist.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Vorgegebene</strong></td>
<td>Legen Sie den Standardeintrag des ProgID-unter Schlüssels auf einen anzeigen Amen für diese ProgID fest, der für den Benutzer geeignet ist. Die Verwendung dieses Eintrags zum Speichern des anzeigen Amens wird durch den Eintrag friendlytykame auf Systemen mit Windows 2000 oder höher als veraltet markiert. Sie sollten diesen Wert jedoch aus Gründen der Abwärtskompatibilität festlegen.<br/></td>
</tr>
<tr class="even">
<td><strong>Allowsilentdefaultübernahme</strong> (eingeführt in Windows 8)</td>
<td>Legen Sie diesen optionalen Eintrag fest, um zu signalisieren, dass Windows diese ProgID ignorieren soll, wenn ein Standard Handler für einen öffentlichen Dateityp bestimmt wird. Unabhängig davon, ob dieser Wert festgelegt ist, wird die ProgID weiterhin im openWith-Kontextmenü und Dialogfeld angezeigt. Dies ist ein REG_NONE Wert.</td>
</tr>
<tr class="odd">
<td><strong>Appusermodelid</strong> (eingeführt in Windows 7)</td>
<td>Legen Sie diesen optionalen Eintrag auf die explizite Anwendungs Benutzer Modell-ID (appusermodelid) der Anwendung fest, wenn die Anwendung eine explizite appusermodelid verwendet und entweder die automatisch generierten <strong>aktuellen</strong> oder <strong>häufigen</strong> Sprung Listen des Systems verwendet oder eine benutzerdefinierte Sprung Liste bereitstellt. Wenn eine Anwendung eine explizite appusermodelid verwendet und diesen Wert nicht festgelegt, werden Elemente nicht in den Sprung Listen dieser Anwendung angezeigt. Dies ist eine REG_SZ Zeichenfolge. Weitere Informationen finden Sie unter <a href="appids.md">App-Benutzer Modell-IDs (appusermudelids)</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>EditFlags</strong></td>
<td>Legen Sie diesen optionalen Eintrag mithilfe von Flags aus der <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>filetypeattributeflags</strong></a> -Enumeration fest. Der EditFlags-Eintrag steuert einige Aspekte der shellverarbeitung der mit dieser ProgID verknüpften Dateitypen. Sie können auch den EditFlags-Eintrag verwenden, um einzuschränken, wie stark der Benutzer bestimmte Aspekte dieser Dateitypen mithilfe des Eigenschaften Blatts einer Datei ändern kann. Die für EditFlags verwendeten <strong>filetypeattributeflags</strong> -Werte sind binäre Werte, die so entworfen wurden, dass Sie mehrere Attribute in einem bitweisen OR-Vorgang zu einem einzelnen Wert zusammenfassen können. Dies ist ein REG_DWORD oder REG_BINARY Wert.<br/></td>
</tr>
<tr class="odd">
<td><strong>Friendlytyname</strong></td>
<td>Legen Sie diesen Eintrag auf einen anzeigen Amen für die ProgID fest, der für den Benutzer geeignet ist. Aus Konsistenz Gründen sollte diese Zeichenfolge die gleichen Daten wie der Standardeintrag für diesen ProgID-Schlüssel enthalten. Dieser Eintrag kann entweder eine REG_SZ oder eine REG_EXPAND_SZ Zeichenfolge sein, muss jedoch als indirekte Zeichenfolge (ein voll qualifizierter Dateiname und Ressourcen Wert mit vorangestelltem @-Symbol) formatiert sein, z.b. <em>@% systemroot% \shell32.dll,-154</em>.<br/></td>
</tr>
<tr class="even">
<td><strong>InfoTip</strong></td>
<td>Legen Sie diesen Eintrag auf eine kurze Hilfe Meldung fest, die von der Shell für diese ProgID angezeigt wird. Der infotip-Eintrag wird in einem Mouseover-Dialogfeld angezeigt. Bei diesem Wert kann es sich entweder um eine REG_SZ oder REG_EXPAND_SZ Zeichenfolge handeln, aber wie friendlytytzame, muss er als indirekte Zeichenfolge formatiert werden.<br/></td>
</tr>
<tr class="odd">
<td><strong>Curver</strong></td>
<td>Legen Sie den (Standard-) Eintrag dieses unter Schlüssels auf die aktuelle Version dieser ProgID fest.<br/>
<blockquote>
[!Note]<br />
Sie sollten die Verwendung von " <strong>Cursor</strong>" vermeiden, es sei denn, Sie haben parallele Anwendungsversionen, d. h. mehrere Versionen, die auf demselben System installiert sind.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>DefaultIcon</strong>.</td>
<td>Legen Sie den (Standard-) Eintrag dieses unter Schlüssels auf das Standard Symbol fest, das für die mit dieser ProgID verknüpften Dateitypen angezeigt werden soll. Dieser Wert kann entweder eine REG_SZ oder eine REG_EXPAND_SZ Zeichenfolge sein, muss jedoch als voll qualifizierter Dateiname mit dem zugehörigen Ressourcen Wert bereitgestellt werden, z.b. <em>% systemroot% \shell32.dll,-154</em>.<br/></td>
</tr>
</tbody>
</table>



 

Im folgenden Beispiel für einen Registrierungsschlüssel wird ein Schlüsselknoten für die Datei Zuordnungs ProgID veranschaulicht:

```
HKEY_CLASSES_ROOT
   Vendor.App.1
      (Default) = My Friendly Name
      AllowSilentDefaultTakeOver
      AppUserModelID = Vendor.Application
      EditFlags = 0x00000001
      FriendlyTypeName = @%SystemRoot%\shell32.dll,-154
      InfoTip = @%SystemRoot%\shell32.dll,-54
      CurVer
         (Default) = Vendor.App.1
      DefaultIcon
         (Default) = %SystemRoot%\shell32.dll,-1
```

## <a name="using-versioned-programmatic-identifiers"></a>Verwenden von programmatischen bezeichlern mit Versions Angabe

Eine mit Versions Angabe versehene ProgID ist eine, deren Version in Ihrem Namen angegeben ist. Dies geschieht in der Regel, indem Sie dem Namen einen Zeitraum und die Versionsnummer hinzufügen. Beispiel:

-   Word.Doc.6
-   Word.Doc.8

Dabei handelt es sich um versionierte ProgIDs mit den Versionen 6 und 8. Wenn Sie über eine parallele Anwendung verfügen, d. h. eine, die mehrere Versionen der Anwendung gleichzeitig installiert unterstützt, verwenden Sie die von currver und Versions unabhängigen ProgIDs. Andernfalls sollten die Dienst-und Versions unabhängigen ProgIDs vermieden werden, da Sie zu Ineffizienz führen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren eines Dateityps für eine neue Anwendung](how-to-register-a-file-type-for-a-new-application.md)
</dt> <dt>

[Anwendungs Registrierung](app-registration.md)
</dt> <dt>

[Dateitypen](fa-file-types.md)
</dt> <dt>

[Funktionsweise von Dateizuordnungen](fa-how-work.md)
</dt> <dt>

[Inhaltsansicht nach Dateityp oder-Art](prophand-content-view.md)
</dt> <dt>

[Dateityp Überprüfung](file-type-verifier.md)
</dt> <dt>

[Dateityp Handler](fa-file-extensions.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> <dt>

[Zuordnungs Arrays](fa-associationarray.md)
</dt> </dl>

 

 




