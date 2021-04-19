---
description: In diesem Artikel wird beschrieben, wie der Filter Graph-Manager einen Quell Filter anhand eines Datei namens eingibt.
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: Registrieren eines benutzerdefinierten Dateityps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e98c01555497ac628fff452f464c826475edbb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342547"
---
# <a name="registering-a-custom-file-type"></a>Registrieren eines benutzerdefinierten Dateityps

In diesem Artikel wird beschrieben, wie der Filter Graph-Manager einen Quell Filter anhand eines Datei namens eingibt. Sie können diesen Mechanismus verwenden, um eigene benutzerdefinierte Dateitypen zu registrieren. Sobald der Dateityp registriert ist, lädt DirectShow automatisch den richtigen Quell Filter, wenn eine Anwendung [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) oder [**igraphbuilder:: addsourcefilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)aufruft.

-   [Übersicht](#overview)
-   [Protokolle](#protocols)
-   [Dateierweiterungen](#file-extensions)
-   [Bytes überprüfen](#check-bytes)
-   [Der Quell Filter wird geladen.](#loading-the-source-filter)
-   [Benutzerdefinierte Dateitypen in Windows Media Player](#custom-file-types-in-windows-media-player)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Um einen Quell Filter anhand eines angegebenen Datei namens zu suchen, versucht der Filter Graph-Manager, die folgenden Schritte in der angegebenen Reihenfolge durchzuführen:

1.  Entspricht dem Protokoll, falls vorhanden.
2.  Mit der Dateierweiterung vergleichen.
3.  Vergleichen Sie die Muster der Bytes in der Datei, die als *Check Bytes* bezeichnet werden.

## <a name="protocols"></a>Protokolle

Protokollnamen wie "FTP" oder "http" werden unter dem

**HKEY- \_ Klassen Stamm \_**

Schlüssel mit der folgenden Struktur:


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



Wenn der Dateiname oder die URL einen Doppelpunkt (': ') enthält, versucht der Filter Graph-Manager, den Teil vor ': ' als Protokollnamen zu verwenden. Wenn der Name beispielsweise "myprot://MyFile.ext" lautet, sucht er nach einem Registrierungsschlüssel mit dem Namen " **myprot**". Wenn dieser Schlüssel vorhanden ist und einen Unterschlüssel mit dem Namen "Extensions" enthält, sucht der Filter Graph-Manager innerhalb des unter Schlüssels nach Einträgen, die der Dateierweiterung entsprechen. Der Wert des Schlüssels muss eine GUID in Form einer Zeichenfolge sein. Beispiel: " {00000000-0000-0000-0000-000000000000} ". Wenn der Filter Diagramm-Manager keine Entsprechungen innerhalb des unter Schlüssels " **Erweiterungen** " aufweisen kann, sucht er nach einem Unterschlüssel namens **Quell Filter**, bei dem es sich auch um eine GUID im Zeichen folgen Format handeln muss.

Wenn der Filter Diagramm-Manager eine übereinstimmende GUID findet, wird diese als CLSID des Quell Filters verwendet, und es wird versucht, den Filter zu laden. Wenn keine Entsprechung gefunden wird, wird der Datei [Quellen Filter (URL)](file-source--url--filter.md) verwendet, der den Dateinamen als URL behandelt.

Dieser Algorithmus hat zwei Ausnahmen:

-   Um Treiber Buchstaben auszuschließen, werden Zeichen folgen mit einem Zeichen nicht als Protokolle betrachtet.
-   Wenn die Zeichenfolge "file:" oder "file://" ist, wird Sie nicht als Protokoll behandelt.

## <a name="file-extensions"></a>Dateierweiterungen

Wenn der Dateiname kein Protokoll enthält, sucht der Filter Graph-Manager in der Registrierung nach Einträgen mit den Schlüssel- **\_ \_ \\ Medientyp \\ Erweiterungen \\** der Schlüssel-HKEY-Klasse.*ext* \\ , wobei.*ext* ist die Dateierweiterung. Wenn dieser Schlüssel vorhanden ist, enthält der Wert **Quell Filter** die CLSID des Quell Filters in Form einer Zeichenfolge. Optional kann der Schlüsselwerte für **Medientyp** und **Untertyp** aufweisen, die den Haupttyp und die Untertyp-GUIDs enthalten.

## <a name="check-bytes"></a>Bytes überprüfen

Einige Dateitypen können durch bestimmte Muster von Bits identifiziert werden, die bei bestimmten Byte Offsets in der Datei auftreten. Der Filter Graph-Manager sucht in der Registrierung nach Schlüsseln in der folgenden Form:

**HKEY \_ Klassen Stamm- \_ \\ mediaType \\**{ *Major Type* } \\ { *Untertyp* }

wobei *Haupttyp* und *Untertyp* GUIDs sind, die den Medientyp für den Bytestream definieren. Jeder Schlüssel enthält einen oder mehrere Unterschlüssel, normalerweise den Namen "1", "2" usw., die die Überprüfung der Bytes definieren. und einen Unterschlüssel namens **Quell Filter** , der die CLSID des Quell Filters in Form von Zeichen folgen enthält. Bei den Check-Byte-unter Schlüsseln handelt es sich um Zeichen folgen, die einen oder mehrere Quads mit dem Namen enthalten:

*Offset*, *CB*, *Maske*, *Val*

Um die Datei abzugleichen, liest der Filter Graph-Manager CB-bytes, beginnend mit dem Byte Nummern Offset. Anschließend wird ein bitweiser And-Operator mit dem Wert in Mask durchführt. Wenn das Ergebnis "Val" ist, ist die Datei für dieses Vierfache gleich. Die Werte mask und Val werden in HEX angegeben. Ein leerer Eintrag für Mask wird als eine Zeichenfolge mit einer Länge von 1 s der Länge CB behandelt. Ein negativer Wert für Offset gibt einen Offset vom Dateiende an. Um den Schlüssel abzugleichen, muss die Datei mit allen Quads in den unter Schlüsseln identisch sein.

Nehmen Sie beispielsweise an, die Registrierung enthält die folgenden Schlüssel unter **HKCR- \\ Medientyp**:


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



Der erste Schlüssel entspricht dem Haupttyp MediaType \_ Stream. Der Unterschlüssel unten, der dem Untertyp "MediaType \_ MIDI" entspricht. Der Wert für den Quell Filter Unterschlüssel ist CLSID \_ asynshader, die CLSID des [Datei Quell Filters (Async)](file-source--async--filter.md) .

Jeder Eintrag kann über mehrere Vierbeiner verfügen. alle müssen abgeglichen werden. Im folgenden Beispiel müssen die ersten 4 Bytes der Datei 0xab, 0xCD, 0x12, 0x34; sein. und die letzten 4 Bytes der Datei müssen 0xab, 0xAB, 0x00, 0xAB lauten:


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



Außerdem können mehrere Einträge unter einem einzelnen Medientyp aufgelistet werden. Eine Entsprechung zu den entsprechenden ist ausreichend. Dieses Schema ermöglicht eine Reihe alternativer Masken; beispielsweise WAV-Dateien, die möglicherweise über einen Riff-Header verfügen.

> [!Note]  
> Dieses Schema ähnelt dem Schema, das von der [**getclassfile**](/windows/win32/api/objbase/nf-objbase-getclassfile) -Funktion verwendet wird.

 

## <a name="loading-the-source-filter"></a>Der Quell Filter wird geladen.

Vorausgesetzt, dass der Filter Graph-Manager einen passenden Quell Filter für die Datei findet, wird dieser Filter dem Diagramm hinzugefügt, der Filter für die [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) -Schnittstelle abgefragt und [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load)aufgerufen. Die Argumente für die **Load** -Methode sind der Dateiname und der Medientyp, wie in der Registrierung festgelegt.

Wenn der Filter Graph-Manager keine Elemente aus der Registrierung finden kann, wird standardmäßig der asynchrone Datei Quell Filter verwendet. In diesem Fall wird der Medientyp auf **mediaType \_ Stream** und **mediasubtype \_ None** festgelegt.

## <a name="custom-file-types-in-windows-media-player"></a>Benutzerdefinierte Dateitypen in Windows Media Player

Windows Media Player verwendet einen zusätzlichen Satz von Registrierungs Einträgen. Weitere Informationen finden Sie unter [Registrierungs Einstellungen für Dateinamen Erweiterungen](../wmp/file-name-extension-registry-settings.md) im Windows Media Player SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 
