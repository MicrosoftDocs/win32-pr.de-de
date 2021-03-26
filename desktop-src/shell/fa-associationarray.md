---
description: Ein Zuordnungs Array ist eine geordnete Liste von Registrierungsstellen, die zum Speichern von Informationen zu einem Elementtyp verwendet werden, einschließlich Handlern, Verben und anderen Attributen, wie z. b. Symbol und Anzeige Name des Typs.
title: Zuordnungs Arrays
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9ECD19CA-833E-4565-A0EF-FB16BF7B3F44
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 75d42a8758e5c6380414c7b93979b4f93cafd013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128888"
---
# <a name="association-arrays"></a>Zuordnungs Arrays

Ein Zuordnungs Array ist eine geordnete Liste von Registrierungsstellen, die zum Speichern von Informationen zu einem Elementtyp verwendet werden, einschließlich Handlern, Verben und anderen Attributen, wie z. b. Symbol und Anzeige Name des Typs. Die Shell verwendet Zuordnungs Arrays, um einen vordefinierten Satz von Registrierungs Speicherorten abzufragen, die möglicherweise Informationen über ein shellelement enthalten.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zu Zuordnungs Arrays](#about-association-arrays)
-   [Abfragen von Zuordnungs Arrays](#querying-association-arrays)
-   [Arbeiten mit Zuordnungs Arrays für eine bestimmte shelldatenquelle](#working-with-association-arrays-for-a-particular-shell-data-source)
    -   [Arrays der Shell-Datenquellen Zuordnung](#shell-data-source-association-arrays)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="about-association-arrays"></a>Informationen zu Zuordnungs Arrays

Ein Zuordnungs Array ist eine geordnete Liste von Registrierungsstellen, die Informationen zu einem Elementtyp enthalten, einschließlich Handlern, Verben und anderen Attributen, wie z. b. Symbol und Anzeige Name des Typs. Diese Informationen zum Elementtyp können auf unterschiedlichen Genauigkeits Graden registriert werden. Beispielsweise können Sie ein Verb registrieren, das nur für einen bestimmten Dateityp (z. b.. jpg) oder für alle Elemente mit dem gleichen System. Kind (z. b. System. Kind = Bild) oder für alle Elemente angezeigt wird.

Die Shell verwendet Zuordnungs Arrays, um einen vordefinierten Satz von Registrierungs Speicherorten abzufragen, die möglicherweise Informationen über das Element enthalten. Die Association Array-APIs können verwendet werden, um aus dem Registrierungs Unterschlüssel einen einzelnen Wert abzurufen, der die angeforderten Informationen enthält. dieser Wert stammt aus dem ersten Eintrag im Array, der ihn bereitstellt. Beispielsweise wird der Standard Symbolwert auf diese Weise abgerufen. Das Association-Array kann auch verwendet werden, um einen Satz von Werten abzurufen, die in den Registrierungs unter Schlüsseln gespeichert werden. Beispielsweise wird die Liste der Verben aus den Verben erstellt, die unter allen unter Schlüsseln registriert sind.

Nachdem die Shell einen vordefinierten Satz von Registrierungs Speicherorten für Informationen über ein shellelement abgefragt hat, werden die Registrierungs Orte von der spezifischsten Position bis zum allgemeinsten in ein Array eingefügt.

Da Zuordnungs Arrays geordnete Listen sind, stellen Sie Anwendungsentwicklern einen Mechanismus zum Hinzufügen von Informationen zur Registrierung zur Verfügung, die für einen bestimmten Elementtyp zurückgegeben werden. Ebenso ermöglichen Zuordnungs Arrays Anwendungsentwicklern das Hinzufügen von Informationen zur Registrierung für eine bestimmte Gruppe von Elementen, wenn diese Elemente an einem allgemeineren Speicherort registriert werden. Diese Logik informiert Sie über den am besten geeigneten Speicherort in der Registrierung, um Informationen zu shellelementen zu speichern.

In einem standardmäßigen Windows-System weist eine JPG-Datei das folgende Zuordnungs Array auf:

-   **HKEY \_ Klassen \_** Stamm- \\ **jpgfile**
-   **HKEY \_ Klassen \_** Stamm \\ **systemfilezuordnungen** \\ **. jpg**
-   **HKEY \_ Klassen \_** Stamm \\ **Bild**
-   **HKEY \_ Klassen \_** Stamm \\ * *\** _
-   _ *HKEY- \_ Klassen \_ root **\\** AllFilesystemObjects**

Informationen zum Registrieren von Zuordnungs Arrays finden Sie unter [Anwendungs Registrierung](app-registration.md).

## <a name="querying-association-arrays"></a>Abfragen von Zuordnungs Arrays

Es gibt Shell-APIs zum Abrufen von Informationen aus einem Bereich von Registrierungs unter Schlüsseln, vom spezifischsten Registrierungs Unterschlüssel zu einer übergeordneten Menge der Informationen für alle Registrierungs Unterschlüssel.

Die häufigste Verwendung eines Zuordnungs Arrays besteht darin, einen einzelnen Wert abzufragen, den die Shell aus dem spezifischsten Element im Array zurückgibt, das über die angeforderten Informationen verfügt. Das folgende Codebeispiel zeigt, wie Sie dies tun.


```
IQueryAssociations *pqa;

// pShellItem is assumed to be an existing IShellItem object.
hr = pShellItem->BindToHandler(NULL, BHID_AssociationArray, IID_PPV_ARGS(&pqa));
if (SUCCEEDED(hr))
{
    wchar_t szValue[256];
    DWORD cbValue = sizeof(szValue);      // Count of bytes in the array

    hr = pqa->GetData(0, ASSOCDATA_VALUE, L"InfoTip", szValue, &cbValue);
    if (SUCCEEDED(hr))
    {
        // The "InfoTip" value is used to compute the infotip string from
        // properties of an item.
    }
    pqa->Release();
}
```



Die folgenden APIs können zum Abfragen eines Zuordnungs Arrays oder zum Erstellen eines Zuordnungs Array- [**iqueryassociation**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Objekts verwendet werden, das abgefragt werden kann:

-   [**Assoccreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (vor Windows Vista)
-   [**Assockreateforclasses**](/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses)
-   [**Assocquerystring**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)

## <a name="working-with-association-arrays-for-a-particular-shell-data-source"></a>Arbeiten mit Zuordnungs Arrays für eine bestimmte shelldatenquelle

Jede shelldatenquelle definiert das Zuordnungs Array für ihre Elemente. Die Definition eines Zuordnungs Arrays ist in der Regel eine Funktion des Elementtyps. Die Implementierer von shelldatenquellen müssen die Zuordnungs Arrays definieren und dokumentieren, damit Anwendungen das Verhalten dieser Typen, z. b. das Registrieren von Verben oder anderen Informationen, erweitern können. Anwendungen können das Verhalten von Elementen erweitern, basierend auf dem Hinzufügen von Daten zu den unter Schlüsseln des Assoziations Arrays, z. b. Hinzufügen von Verben für Elemente

Die Dateisystem-Datenquelle erstellt ein Zuordnungs Array für Dateien, die auf den folgenden Registrierungs unter Schlüsseln und speziellen ProgIDs basieren:

-   Wenn die Datei eine registrierte ProgID hat, wird die Stamm-ProgID der **HKEY- \_ Klassen \_** \\  verwendet. Andernfalls wird der Stamm der **HKEY- \_ Klassen \_**" \\ **Unknown** " verwendet.
-   Die Dateinamenerweiterung wird unter **HKEY \_ Classes \_ root** \\ **systemfileassociations** \\ *. FileExtension* unter Key registriert.
-   In der folgenden Tabelle sind spezielle ProgIDs aufgeführt. 

    | Besondere ProgID                                    | BESCHREIBUNG                   |
    |---------------------------------------------------|-------------------------------|
    | **HKEY \_ Klassen \_** Stamm \\ * *\** _                   | Alle Dateien (nicht-Ordner)       |
    | _ *HKEY- \_ Klassen \_ root **\\** AllFilesystemObjects** | Dateien und Dateisystem Ordner |
    | **HKEY \_ Klassen \_** Stamm \\ **Verzeichnis**            | Dateisystem Ordner           |
    | **HKEY \_ Klassen \_** Stamm \\ **Ordner**               | Shellcontainer              |

    

     

### <a name="shell-data-source-association-arrays"></a>Arrays der Shell-Datenquellen Zuordnung

In der folgenden Liste sind einige der Arrays für die Shell-Datenspeicher Zuordnung dargestellt, die für die in diesem Thema beschriebenen Zwecke verwendet werden können:

-   **HKEY \_ Klassen \_** Stamm \\ * *\** _
-   _ *HKEY- \_ Klassen \_ root **\\** AllFilesystemObjects**
-   **HKEY \_ Klassen \_** StammKind.Doc-Enumerationselement \\ ****
-   **HKEY \_ Klassen \_** Stamm \\ **Ergebnisse**
-   **HKEY \_ Klassen \_** Stamm \\ **systemfilezuordnungen** \\ **. docx**
-   **HKEY \_ Klassen \_** StammWord.Doc-Enumerationselement \\ **. 12**

Arrays der Shell-Datenquellen Zuordnung, die für dbfolder (ein shelldatenspeicher, der Elemente in Suchergebnissen und Abfrage basierten Sichten darstellt) verwendet werden können, lauten wie folgt:

-   Laufwerke
-   Netzwerk
-   Regitems
-   Beispiele:
    -   ContentView
    -   Verben

Andere allgemeine Zuordnungs Arrays enthalten Ordner und Drucker.

## <a name="additional-resources"></a>Weitere Ressourcen

-   Informationen zum Erstellen eines Shell-Datenspeicher finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](nse-implement.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

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

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> </dl>

 

 
