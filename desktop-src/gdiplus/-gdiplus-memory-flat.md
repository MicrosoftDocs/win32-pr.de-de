---
description: Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Speicherfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e748f8a68cc6f04deba3c9676638ee48ee2e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978985"
---
# <a name="memory-functions"></a>Speicherfunktionen

Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind. Die Funktionen in der flatapi GDI+ werden von einer Sammlung von ungefähr 40 C++-Klassen umschließt. Es wird empfohlen, die Funktionen in der flatapi nicht direkt aufzurufen. Wenn Sie GDI+ aufrufen, sollten Sie dies tun, indem Sie die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden. Der Microsoft-Produktsupport bietet keine Unterstützung für Code, mit dem die flatapi direkt aufgerufen wird. Weitere Informationen zur Verwendung dieser Wrapper Methoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Die folgenden flatapi-Funktionen werden von der [**gdiplus Base**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++-Klasse umschließt.

## <a name="memory-functions-and-corresponding-wrapper-methods"></a>Speicherfunktionen und entsprechende Wrapper Methoden



| Flat-Funktion                                          | Wrapper Methode                                                                                                                                      | Bemerkungen                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Gpstatus wingdipapi gdipalloc (Größe \_ t-Größe)<br/> | [**Gpstatus wingdipapi gdiplusbase void \* (Operator new) (Größe \_ t in \_ Größe)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | Belegt Speicher für ein Windows-GDI+-Objekt. <br/> Gdipalloc ist in "gdipl. h" deklariert.<br/>  |
| Gpstatus wingdipapi gdipfree (void \* PTR);<br/>   | [**Gpstatus wingdipapi gdiplusbase void (Operator Delete) (void \* in \_ pVoid)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | Hebt die Zuordnung von Arbeitsspeicher für ein Windows-GDI+-Objekt auf. <br/> Gdipfree ist in "gdipl. h" deklariert.<br/> |



 

 

 
