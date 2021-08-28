---
description: Ein Handle für eine Windows Runtime-Zeichenfolge.
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: HSTRING (Hstring.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b43c92d439cec10c0d1683efb1e8ceafd8165a35c3c8aa9a1b35150e43a33a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121570"
---
# <a name="hstring"></a>HSTRING

Ein Handle für eine Windows Runtime-Zeichenfolge.


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a>Hinweise

Verwenden **Sie HSTRING,** um unveränderliche Zeichenfolgen in der Windows darstellen.

JavaScript und andere Sprachen wie C und Microsoft Visual Basic können Zeichenfolgen verwenden, die mithilfe von \# **HSTRING dargestellt werden.** Die folgende Tabelle zeigt, wie **HSTRING** in anderen Sprachen dargestellt wird.



| Programmiersprache                                                                    | Zeichenfolgendarstellung                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | [winrt::hstring-Klasse](/uwp/cpp-ref-for-winrt/hstring)     |
| Visual C++ Komponentenerweiterungen ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx)) | [Platform::String-Klasse](/cpp/cppcx/platform-string-class) |
| JavaScript                                                                              | String-Objekt                                              |
| .NET Framework                                                                          | System.String-Klasse                                        |



 

Das **HSTRING-Handle** ist ein Standardhandpunkttyp. Semantisch stellt **ein HSTRING-Objekt,** das den Wert **NULL** enthält, die leere Zeichenfolge dar, die aus null Inhaltszeichen und einem beendenden **NULL-Zeichen** besteht. Das Erstellen einer Zeichenfolge [**über WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) mit 0 Zeichen erzeugt den Handlewert **NULL.** Beim Aufrufen [**von WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) mit dem Wert **NULL** wird ein Zeiger auf eine leere Zeichenfolge gefolgt von nur dem **NUL-Abschlusszeichen** zurückgegeben. Es ist kein eindeutiger Wert vorhanden, um eine nicht initialisierte **HSTRING-Datei** zu darstellen.

Rufen Sie [**die WindowsCreateString-Funktion**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) auf, um eine neue **HSTRING-Funktion** zu erstellen, und rufen Sie die [**WindowsDeleteString-Funktion**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) auf, um den Verweis auf den Speicher der sichernden Zeichenfolge frei zu geben. Rufen Sie [**die WindowsCreateStringReference-Funktion auf,**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) um einen Zeichenfolgenverweis zu erstellen, der auch als *FastPass-Zeichenfolge bezeichnet wird.*

Kopieren Sie **eine HSTRING-Datei,** indem Sie [**die WindowsDuplicateString-Funktion**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) aufrufen.

Verketten Sie zwei Zeichenfolgen, indem Sie die [**WindowsConcatString-Funktion**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) aufrufen.

Greifen Sie auf den Speicher der hintergrundenden Zeichenfolge zu, indem Sie die [**WindowsGetStringRawBuffer-Funktion**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) aufrufen.

**HSTRING kann** eingebettete **NUL-Zeichen** speichern und verwenden. Verwenden Sie [**die WindowsStringHasEmbeddedNull-Funktion,**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) um nach eingebetteten **NUL-Zeichen** zu überprüfen, bevor Sie Funktionen verwenden, die zu unerwarteten Ergebnissen führen können. Beispielsweise verwenden die meisten **Windows-Funktionen LPCWSTR** als Eingabeparameter und berechnen die Länge der Zeichenfolge nur, bis die erste **NUL** gefunden wird.

Die Zeichenfolge muss unveränderlich und mit NULL beendet bleiben. Wenn beim Aufrufen von Code mithilfe der [**WindowsCreateStringReference-Funktion**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) ein Zeichenfolgenverweis erstellt wird, befindet sich der Arbeitsspeicher, der die Zeichenfolgendarstellung enthält, im Besitz des Aufrufers. Die Windows Runtime basiert darauf, dass der Inhalt der ursprünglichen Zeichenfolge unverändert bleibt. Beim Übergeben eines Zeichenfolgenverweises an die Windows Runtime ist der Aufrufer dafür verantwortlich, sicherzustellen, dass der Inhalt der Zeichenfolge unveränderlich ist und **NUL** für die Dauer des Aufrufs beendet wird. Die Windows Runtime gibt alle Verweise auf den Zeichenfolgenverweis frei, wenn der Aufruf zurückgegeben wird.

Wenn Sie **HSTRING als** out-Parameter erhalten, ist es eine bewährte Methode, das Handle auf **NULL** zu setzen, wenn Sie damit fertig sind.

Rufen Sie [**die Funktion WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) auf, um einen änderbaren Zeichenfolgenpuffer zu reservieren, den Sie zum Erstellen eines unveränderlichen **HSTRING verwenden können.** Wenn Sie das Aufpopulieren des Puffers abgeschlossen haben, rufen Sie die [**WindowsPromoteStringBuffer-Funktion**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) auf, um **HSTRING zu erstellen.** Dieses Zweiphasen-Konstruktionsmuster ermöglicht Funktionen, die einem "Zeichenfolgen-Generator" ähneln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| Header<br/>                   | <dl> <dt>Hstring.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>


</dt> <dt>

[**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring)
</dt> <dt>

[**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring)
</dt> <dt>

[**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)
</dt> <dt>

[**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> </dl>

 

 
