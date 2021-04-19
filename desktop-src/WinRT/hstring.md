---
description: Ein Handle für eine Windows-Runtime Zeichenfolge.
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: Hstring (hstring. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9e73d7627a4bab8f02a95056e5b208569d922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348398"
---
# <a name="hstring"></a>HSTRING

Ein Handle für eine Windows-Runtime Zeichenfolge.


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a>Bemerkungen

Verwenden Sie **hstring** , um unveränderliche Zeichen folgen in der Windows-Runtime darzustellen.

In JavaScript und anderen Sprachen, wie z. b. C \# und Microsoft Visual Basic, können Zeichen folgen verwendet werden, die mithilfe von **hstring** dargestellt werden. In der folgenden Tabelle wird gezeigt, wie ein **hstring** in anderen Sprachen dargestellt wird.



| Programmiersprache                                                                    | Zeichen folgen Darstellung                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | [WinRT:: hstring](/uwp/cpp-ref-for-winrt/hstring) -Klasse     |
| Komponenten Erweiterungen für Visual C++ ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx)) | [Platform:: String](/cpp/cppcx/platform-string-class) -Klasse |
| JavaScript                                                                              | String-Objekt                                              |
| .NET Framework                                                                          | System.String-Klasse                                        |



 

Das **hstring** -Handle ist ein Standard behandlertyp. Semantisch stellt ein **hstring** , der den Wert **null** enthält, die leere Zeichenfolge dar, die aus keinem Inhalts Zeichen und einem abschließenden **null** -Zeichen besteht. Das Erstellen einer Zeichenfolge über [**windowscreatestring**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) mit NULL Zeichen erzeugt den Handle-Wert **null**. Beim Aufrufen von [**windowsgetstringrawbuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) mit dem Wert **null** wird ein Zeiger auf eine leere Zeichenfolge zurückgegeben, auf die nur das Zeichen für das abschließende **NUL** -Zeichen folgt. Es gibt keinen eindeutigen Wert, der einen nicht initialisierten **hstring** darstellt.

Rufen Sie die [**windowscreatestring**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) -Funktion auf, um einen neuen **hstring**-Code zu erstellen, und rufen Sie die [**windowsdeletestring**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) -Funktion auf, um den Verweis auf den Zeichen folgen Speicher für die Rufen Sie die [**windowscreatestrauch ingreferenzierungsfunktion**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) auf, um einen Zeichen folgen Verweis zu erstellen. dieser wird auch als *fast-Pass-Zeichenfolge* bezeichnet.

Kopieren Sie ein **hstring-Zeichen** , indem Sie die [**windowsduplicatestring**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) -Funktion aufrufen.

Verkettet zwei Zeichen folgen durch Aufrufen der [**windowsconcatstring**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) -Funktion.

Greifen Sie über die [**windowsgetstringrawbuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) -Funktion auf den Speicher für die Unterstützungs Zeichenfolge zu.

**Hstring** kann eingebettete **NUL** -Zeichen speichern und verwenden. Verwenden Sie die [**windowsstringhasembeddednull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) -Funktion, um vor der Verwendung von Funktionen, die möglicherweise unerwartete Ergebnisse verursachen, nach eingebetteten **NUL** -Zeichen zu suchen. Beispielsweise verwenden die meisten Windows-Funktionen **LPCWSTR** als Eingabeparameter und berechnen die Länge der Zeichenfolge nur, bis die erste **NUL** erreicht wird.

Die Unterstützungs Zeichenfolge muss unveränderlich und NULL-terminiert bleiben. Wenn der aufrufende Code einen Zeichen folgen Verweis mithilfe der [**windowscreatestrauferenferenzierungsfunktion**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) erstellt, befindet sich der Arbeitsspeicher, der die zugrunde liegende Zeichen folgen Darstellung enthält, dem Aufrufer. Der Windows-Runtime der den Inhalt der ursprünglichen Zeichenfolge verlässt, bleibt unverändert. Wenn Sie einen Zeichen folgen Verweis an den Windows-Runtime übergeben, liegt es in der Verantwortung des Aufrufers sicherzustellen, dass sich der Inhalt der Zeichenfolge ändert und die **NUL** für die Dauer des Aufrufes beendet wird. Der Windows-Runtime gibt alle Verweise auf den Zeichen folgen Verweis frei, wenn der-Rückruf zurückgegeben wird.

Wenn Sie ein **hstring** als out-Parameter erhalten, empfiehlt es sich, das Handle auf **null** festzulegen, wenn Sie damit fertig sind.

Rufen Sie die [**windowshalallocatestringbuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) -Funktion auf, um einen änderbaren Zeichen folgen Puffer zuzuweisen, den Sie zum Erstellen eines unveränderlichen **hstring** verwenden können. Wenn Sie das Auffüllen des Puffers abgeschlossen haben, rufen Sie die [**windowspromotestringbuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) -Funktion auf, um den **hstring** zu erstellen. Dieses zweistufige Konstruktionsmuster ermöglicht eine ähnliche Funktionalität wie ein "String Builder".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| Header<br/>                   | <dl> <dt>Hstring. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>


</dt> <dt>

[**Windowscreatestring**](/windows/win32/api/winstring/nf-winstring-windowscreatestring)
</dt> <dt>

[**Windowsdeletestring**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring)
</dt> <dt>

[**Windowsduplicatestring**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)
</dt> <dt>

[**Windowshalzugecatestringbuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> </dl>

 

 
