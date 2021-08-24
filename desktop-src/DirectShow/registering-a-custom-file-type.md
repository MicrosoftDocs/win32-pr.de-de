---
description: In diesem Artikel wird beschrieben, wie Graph-Manager einen Quellfilter bei einem Dateinamen sucht.
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: Registrieren eines benutzerdefinierten Dateityps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd2815748fafaff3e2d20d0de1ab5fa0bcc9dec62f4e65ffbdd8479fec434d99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697050"
---
# <a name="registering-a-custom-file-type"></a>Registrieren eines benutzerdefinierten Dateityps

In diesem Artikel wird beschrieben, wie Graph-Manager einen Quellfilter bei einem Dateinamen sucht. Sie können diesen Mechanismus verwenden, um Ihre eigenen benutzerdefinierten Dateitypen zu registrieren. Sobald der Dateityp registriert ist, wird von DirectShow automatisch der richtige Quellfilter geladen, wenn eine Anwendung [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) oder [**IGraphBuilder::AddSourceFilter aufruft.**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)

-   [Übersicht](#overview)
-   [Protokolle](#protocols)
-   [Dateierweiterungen](#file-extensions)
-   [Bytes überprüfen](#check-bytes)
-   [Laden des Quellfilters](#loading-the-source-filter)
-   [Benutzerdefinierte Dateitypen in Windows Media Player](#custom-file-types-in-windows-media-player)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Um einen Quellfilter aus einem bestimmten Dateinamen zu suchen, versucht der Graph-Manager folgende Schritte in der angegebenen Reihenfolge:

1.  Übereinstimmung mit dem Protokoll, falls dies der Fall ist.
2.  Übereinstimmung mit der Dateierweiterung.
3.  Übereinstimmungsmuster von Bytes in der Datei, die als *Prüfbytes bezeichnet werden.*

## <a name="protocols"></a>Protokolle

Protokollnamen wie "ftp" oder "http" werden unter registriert.

**HKEY \_ CLASSES \_ ROOT**

key mit der folgenden Struktur:


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



Wenn der Dateiname oder die URL einen Doppelpunkt (':') enthält, versucht der Filter-Graph-Manager, den Teil vor dem ":" als Protokollnamen zu verwenden. Wenn der Name beispielsweise "myprot://myfile.ext" ist, wird nach einem Registrierungsschlüssel namens **myprot gesucht.** Wenn dieser Schlüssel vorhanden ist und einen Unterschlüssel namens "Extensions" enthält, sucht der Filter Graph Manager innerhalb dieses Unterschlüssels nach Einträgen, die mit der Dateierweiterung übereinstimmen. Der Wert des Schlüssels muss eine GUID in Zeichenfolgenform sein. Beispiel: " {00000000-0000-0000-0000-000000000000} ". Wenn der Filter Graph-Manager keine Übereinstimmungen innerhalb des Unterschlüssels **Erweiterungen** finden kann, sucht er nach einem Unterschlüssel namens **Quellfilter,** der ebenfalls eine GUID in Zeichenfolgenform sein muss.

Wenn der Filter Graph-Manager eine entsprechende GUID findet, verwendet er diese als CLSID des Quellfilters und versucht, den Filter zu laden. Wenn keine Übereinstimmung findet, wird der Filter Dateiquelle [(URL)](file-source--url--filter.md) verwendet, der den Dateinamen als URL behandelt.

Es gibt zwei Ausnahmen von diesem Algorithmus:

-   Um Treiberbuchstaben auszuschließen, werden Zeichenfolgen mit nur einem Zeichen nicht als Protokolle betrachtet.
-   Wenn die Zeichenfolge "file:" oder "file://" ist, wird sie nicht als Protokoll behandelt.

## <a name="file-extensions"></a>Dateierweiterungen

Wenn der Dateiname kein Protokoll enthält, sucht der Filter-Graph-Manager in der Registrierung nach Einträgen mit dem Schlüssel **HKEY \_ CLASSES ROOT Media Type \_ \\ \\ Extensions \\**.*ext* \\ , wobei .*ext* ist die Dateierweiterung. Wenn dieser Schlüssel vorhanden ist, enthält der Wert **Quellfilter** die CLSID des Quellfilters in Zeichenfolgenform. Optional kann der Schlüssel Werte für **Medientyp** und **Untertyp** enthalten, die den Haupttyp und die Untertyp-GUIDs enthalten.

## <a name="check-bytes"></a>Bytes überprüfen

Einige Dateitypen können durch bestimmte Bitmuster identifiziert werden, die an bestimmten Byteoffsets in der Datei auftreten. Der Filter Graph-Manager sucht in der Registrierung nach Schlüsseln im folgenden Formular:

**HKEY \_ CLASSES \_ ROOT \\ MediaType \\**{ *Haupttyp* } \\ { *Untertyp* }

Dabei *sind Haupttyp* *und Untertyp* GUIDs, die den Medientyp für den Bytestream definieren. Jeder Schlüssel enthält einen oder mehrere Unterschlüssel( normalerweise mit den Namen 1, 2 und so weiter), die die Überprüfungsbytes definieren. und einen Unterschlüssel mit dem Namen **Quellfilter,** der die CLSID des Quellfilters in Zeichenfolgenform angibt. Die Check-Byte-Unterschlüssel sind Zeichenfolgen, die ein oder mehrere Quads von Zahlen namens enthalten:

*offset*, *cb*, *mask*, *val*

Um mit der Datei zu übereinstimmen, liest der Graph-Manager cb-Bytes, beginnend mit dem Bytezahlenoffset. Anschließend wird ein bitweises AND für den Wert in der Maske verwendet. Wenn das Ergebnis gleich val ist, entspricht die Datei diesem Quader. Die Werte mask und val werden im Hexadezimalformat angegeben. Ein leerer Eintrag für mask wird als Zeichenfolge der Länge 1 von cb behandelt. Ein negativer Wert für offset gibt einen Offset vom Ende der Datei an. Um mit dem Schlüssel zu übereinstimmen, muss die Datei mit allen Quads in einem der Unterschlüssel übereinstimmen.

Angenommen, die Registrierung enthält die folgenden Schlüssel unter **\\ HKCR-Medientyp:**


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



Der erste Schlüssel entspricht dem Haupttyp MEDIATYPE \_ Stream. Der untere Unterschlüssel, der dem Untertyp MEDIATYPE \_ Format entspricht. Der Wert für den Unterschlüssel Quellfilter ist CLSID \_ AsyncReader, die CLSID des Filters [Dateiquelle (Async).](file-source--async--filter.md)

Jeder Eintrag kann mehrere Vierfache haben. alle müssen übereinstimmen. Im folgenden Beispiel müssen die ersten 4 Bytes der Datei 0xAB, 0xCD, 0x12, 0x34; und die letzten 4 Bytes der Datei müssen 0xAB, 0xAB, 0x00, 0xAB:


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



Darüber hinaus können mehrere Einträge unter einem einzelnen Medientyp aufgeführt sein. Eine Übereinstimmung mit einer dieser Beiden ist ausreichend. Dieses Schema ermöglicht eine Reihe alternativer Masken. Beispiel: WAV-Dateien, die möglicherweise über einen HEADER VOM-Header verfügen oder nicht.

> [!Note]  
> Dieses Schema ähnelt dem Schema, das von der [**GetClassFile-Funktion verwendet**](/windows/win32/api/objbase/nf-objbase-getclassfile) wird.

 

## <a name="loading-the-source-filter"></a>Laden des Quellfilters

Angenommen, der Filter-Graph-Manager findet einen übereinstimmenden Quellfilter für die Datei, fügt diesen Filter dem Diagramm hinzu, fragt den Filter nach der [**IFileSourceFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) ab und ruft [**IFileSourceFilter::Load auf.**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) Die Argumente für die **Load-Methode** sind der Dateiname und der Medientyp, wie von der Registrierung festgelegt.

Wenn der Filter Graph-Manager nichts aus der Registrierung finden kann, wird standardmäßig der Filter asynchrone Dateiquelle verwendet. In diesem Fall wird der Medientyp auf **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ None festgelegt.**

## <a name="custom-file-types-in-windows-media-player"></a>Benutzerdefinierte Dateitypen in Windows Media Player

Windows Media Player verwendet einen zusätzlichen Satz von Registrierungseinträgen. Weitere Informationen finden Sie unter [File Name Extension Registry Einstellungen](../wmp/file-name-extension-registry-settings.md) im Windows Media Player SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 
