---
description: Arbeiten mit DVD-Text Zeichenfolgen
ms.assetid: 6d415ebb-5cd0-4631-9404-f2ebabef2476
title: Arbeiten mit DVD-Text Zeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d04a786e46c795f028edbe2b955e71715aaefb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368174"
---
# <a name="working-with-dvd-text-strings"></a>Arbeiten mit DVD-Text Zeichenfolgen

Einige DVD-Datenträger, insbesondere CDs-Datenträger, enthalten möglicherweise eine Liste mit Text Zeichenfolgen, um den Video-oder Audioinhalt zu ergänzen Diese Text Zeichenfolgen enthalten Metadaten zum Inhalt, z. b. Titel Titel, Künstlernamen, Genre Informationen usw. Text Zeichenfolgen können in mehr als einer Sprache vorhanden sein. Diese Zeichen folgen sind optional, und viele CDs verfügen nicht über diese Zeichen folgen.

Wenn Sie Text Zeichenfolgen aus einer DVD abrufen möchten, verwenden Sie die [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) -Schnittstelle, die vom [DVD-Navigator](dvd-navigator-filter.md)verfügbar gemacht wird. Es ist nicht erforderlich, ein DVD-Wiedergabe Diagramm zu erstellen, um die Text Zeichenfolgen abzurufen. Sie können einfach den DVD-Navigator erstellen, das DVD-Volume festlegen und dann die entsprechenden Textzeichen folgen Methoden aufzurufen:



| Methode                                                                                  | BESCHREIBUNG                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDvdInfo2:: getdvdtextnumoflanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) | Ruft die Anzahl der Sprachen ab, für die Text Zeichenfolgen vorhanden sind.                                                                                                                                  |
| [**IDvdInfo2:: getdvdtextlanguageinfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo)           | Ruft Informationen zu den Text Zeichenfolgen für eine Sprache ab.                                                                                                                                       |
| [**IDvdInfo2:: getdvdtextstringasunicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)     | Ruft eine Text Zeichenfolge für eine angegebene Sprache nach Index ab.                                                                                                                                          |
| [**IDvdInfo2:: getdvdtextstringasnative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)       | Ruft eine Text Zeichenfolge als rohbytearray ab. Verwenden Sie diese Methode, wenn die Text Zeichenfolge eine Zeichencodierung verwendet, die von [**getdvdtextstringasunicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)nicht unterstützt wird. |



 

Dies ist das grundlegende Verfahren zum erhalten von Text Zeichenfolgen:

1.  Aufrufen von [**IDvdInfo2:: getdvdtextnumoflanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) zum Ermitteln der Gesamtzahl der Sprachen, in denen die Text Zeichenfolgen angezeigt werden. Wenn die Zahl 0 (null) ist, bedeutet dies, dass die DVD keine Text Zeichenfolgen enthält. (Dies ist möglicherweise der häufigste Fall.)
2.  Wenn die Anzahl der Sprachen mindestens 1 ist, wenden Sie sich an [**IDvdInfo2:: getdvdtextlanguageinfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) , um Informationen zu den einzelnen Sprachen zu erhalten. Die Sprache wird durch den Index angegeben. Die-Methode gibt die Gesamtanzahl von Text Zeichenfolgen in dieser Sprache, den Gebiets Schema Bezeichner (**LCID**) für die Sprache und die Zeichencodierung (Unicode oder andere) zurück. Für DVD-Text Zeichenfolgen können mehrere verschiedene Zeichensätze verwendet werden. Diese werden in der [**DVD- \_ textcharset-Enumeration**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset)aufgelistet.
3.  Um eine Text Zeichenfolge abzurufen, wenden Sie [**IDvdInfo2:: getdvdtextstringasunicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) oder [**IDvdInfo2:: getdvdtextstringasnative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)an. Die erste Methode gibt eine Zeichenfolge mit breit Zeichen zurück, unterstützt jedoch nicht jeden Zeichensatz. Die zweite Methode gibt ein Bytearray zurück, das die unformatierten Textdaten enthält. Für beide Methoden können Sie die-Methode mit einem **null** -Puffer Zeiger aufzurufen, um die Größe der Zeichenfolge und den Texttyp zu ermitteln. Weisen Sie dann einen Puffer zu, und wiederholen Sie die Methode, um die Zeichenfolge abzurufen.

Jede Text Zeichenfolge verfügt über einen zugeordneten bezeichnercode, der die Bedeutung der Text Zeichenfolge angibt. Der Bezeichner wird als ein [**DVD- \_ textstringtype**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) -Wert zurückgegeben. Es gibt zwei Kategorien von *Bezeichnern*: *Struktur* Bezeichner und Inhalts Bezeichner. Struktur Bezeichner verfügen über numerische Codes im Bereich 0x00 – 0x02f. Inhalts Bezeichner haben einen Bereich von 0x30 und höher. (Die **DVD- \_ textstringtype** -Enumeration definiert eine Teilmenge der gängigsten Bezeichner, aber die [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) -Methoden können jeden bezeichnercode zurückgeben.) Ein Struktur Bezeichner beschreibt einen logischen Teil der DVD, z. b. Volume, Titel oder Teil des Titels (PTT). Ein Inhalts Bezeichner gibt die Bedeutung einer bestimmten Text Zeichenfolge an, z. b. Filmtitel, Titel oder Genre.

Struktur Bezeichner sind keine Text Zeichenfolgen zugeordnet. Wenn ein Struktur Bezeichner in den Text Zeichenfolgen-Daten angezeigt wird, signalisiert er, dass die folgenden Text Zeichenfolgen für diesen logischen Teil der DVD gelten, bis zum nächsten Struktur Bezeichner. Die Position der Struktur Bezeichner innerhalb der Textdaten entspricht der logischen Hierarchie des DVD-Volumes. Beispielsweise stellt das erste Vorkommen des DVD- \_ Struktur \_ Titel Bezeichners (0x02) den ersten Titel im Volume dar, und das nächste Vorkommen stellt den zweiten Titel dar.

In der folgenden Tabelle wird gezeigt, wie die Text Zeichenfolgen für eine DVD mit zwei Titeln definiert werden können.



| DVD- \_ textstringtype        | Textzeichenfolge  | BESCHREIBUNG                                    |
|----------------------------|--------------|------------------------------------------------|
| DVD- \_ Struktur \_ Volume (0x01) | ""           | Struktur Bezeichner für die gesamte Seiten Seite. |
| Allgemeiner DVD- \_ \_ Name (0x30)  | "DVD-Volume" | Der Name des DVD-Volumes.                               |
| Titel der DVD- \_ Struktur \_ (0x02)  | ""           | Struktur Bezeichner für den ersten Titel.      |
| Allgemeiner DVD- \_ \_ Name (0x30)  | "Titel 1"    | Der Name des ersten Titels.                       |
| Titel der DVD- \_ Struktur \_ (0x02)  | ""           | Struktur Bezeichner für den zweiten Titel.     |
| Allgemeiner DVD- \_ \_ Name (0x30)  | "Title 2"    | Der Name des zweiten Titels.                      |



 

Die Methoden [**getdvdtextstringasunicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) und [**getdvdtextstringasnative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) behandeln Struktur Bezeichner und Inhalts Bezeichner identisch. Der einzige Unterschied besteht darin, dass der zugeordnete Text Puffer für Struktur Bezeichner leer ist. Es liegt an der Anwendung, die Beziehung zwischen den Text Zeichenfolgen und den logischen Teilen der DVD nachzuverfolgen.

Im folgenden Beispiel wird gezeigt, wie Sie Text Zeichenfolgen aus einer DVD erhalten. In diesem Beispiel werden einige Details ignoriert, die für eine echte Anwendung erforderlich sind. (Er ignoriert z. b. Struktur Bezeichner.) Das Beispiel dient nur dazu, die richtige Sequenz von Aufrufen anzuzeigen.


```C++
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }
#define SAFE_ARRAY_DELETE(x) { if (x != NULL) { delete [] x; x = NULL; } }

HRESULT GetDVDTextStrings()
{
    HRESULT hr = S_OK;
    ULONG cLangs = 0;       // Number of languages.
    ULONG cStrings = 0;     // Number of text strings.
    ULONG cchBuffer = 0;    // Buffer size.
    ULONG cchActual = 0;    // Actual string size.

    LCID lcid;              // Locale identifier.
    DVD_TextCharSet     characterSet;
    DVD_TextStringType  stringType;

    WCHAR *pszBuffer = NULL;

    CComPtr<IBaseFilter> pFilter;
    CComPtr<IDvdInfo2> pInfo;
    CComPtr<IDvdControl2> pControl;

    // Set up the DVD Navigator.
    CHECK_HR(hr = pFilter.CoCreateInstance(CLSID_DVDNavigator));
    CHECK_HR(hr = pFilter.QueryInterface(&pInfo));
    CHECK_HR(hr = pFilter.QueryInterface(&pControl));
    CHECK_HR(hr = pControl->SetDVDDirectory(NULL));

    // Find the number of text-string languages.
    CHECK_HR(hr = pInfo->GetDVDTextNumberOfLanguages(&cLangs));
    if (cLangs == 0)
    {
        return S_FALSE; // No text strings.
    }

    // Get information about the 0'th language.
    CHECK_HR(hr = pInfo->GetDVDTextLanguageInfo(
        0, &cStrings, &lcid, &characterSet));

    // First check if this character set is compatible with the 
    // GetDVDTextStringAsUnicode method.

    if (characterSet == DVD_CharSet_Unicode || 
        characterSet == DVD_CharSet_ISO646)
    {
        // Loop through all of the strings.
        for (ULONG i = 0; i < cStrings; i++)
        {
            // Get the i'th string for the 0'th language.

            // Find the required buffer size and the string type.
            CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                0,            // Language index.
                i,            // String index.
                NULL,         // Pass NULL pointer to get the buffer size.
                0,            // Size of the buffer we are passing in.
                &cchBuffer,   // Receives the required buffer size.
                &stringType   // Receives the identifier code.
                ));

            // Skip structure identifiers (0x00 - 0x2F).
            if ((cchBuffer > 0) && (stringType >= 0x30))
            {
                // Allocate a buffer and get the text string.
                pszBuffer = new WCHAR[cchBuffer];
                if (pszBuffer == NULL)
                {
                    CHECK_HR(hr = E_OUTOFMEMORY);
                }

                CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                    0, i, pszBuffer, cchBuffer, &cchActual, &stringType));

                // TODO: Display the text string.

                SAFE_ARRAY_DELETE(pszBuffer);
            }
        }
    }

done:
    SAFE_ARRAY_DELETE(pszBuffer);
    return hr;
}
```



Informationen zu DVD-Text Zeichenfolgen finden Sie auf der [Website des DVD-Forums](https://go.microsoft.com/fwlink/?LinkId=8677).

Die **cdvdcore:: getdvdtext** -Methode in der dvdsample-Anwendung veranschaulicht die grundlegenden Schritte beim Auflisten und Anzeigen von DVD-Text Zeichenfolgen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



