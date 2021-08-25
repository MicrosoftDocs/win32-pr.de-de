---
title: Marshallen von OLE-Datentypen
description: Marshallen von Automatisierungs- und OLE-Datentypen.
ms.assetid: 0cab4208-d40d-40a1-88f2-4933b52c0c29
keywords:
- MIDL und COM MIDL , Marshalling von OLE-Datentypen
- Marshalling von MIDL
- MIDL für OLE-Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91c5f1527ffaa361b85550941af1538c99251e59750b27f3bfe7552251e821e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895020"
---
# <a name="marshaling-ole-data-types"></a>Marshallen von OLE-Datentypen

Um die Verwendung bestimmter Automatisierungs- und OLE-Datentypen sowie einiger häufig in COM verwendeter Systemhandles zu vereinfachen, stehen Typedefs für diese Datentypen und die zugehörigen Hilfsfunktionen zur Verfügung, indem Windows IDL-Dateien importiert und mit den OLE- und Automation DLL-Dateien verknüpft werden. Diese Dateien werden automatisch auf Ihrem System installiert.

-   Um den [**BSTR-Datentyp**](/previous-versions/windows/desktop/automat/bstr) in Remoteprozeduraufrufen zu verwenden, importieren Sie die Datei wtypes.idl in Ihre IDL-Datei (Interface Definition), und verknüpfen Sie sie beim Erstellen Ihrer verteilten Anwendung mit Oleaut32.lib. Dadurch können Ihre Stubs die vorgefertigten Hilfsfunktionen **BSTR \_ UserSize,** **BSTR \_ UserMarshal,** **BSTR \_ UserUnmarshal** und **BSTR \_ UserFree** verwenden.
-   Um andere Automation-Datentypen wie [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) und [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray)oder Typen zu verwenden, die diese Typen verwenden (z. B. [**DISPPARAMS**](/windows/win32/api/oaidl/ns-oaidl-dispparams) und [**EXCEPINFO),**](/windows/win32/api/oaidl/ns-oaidl-excepinfo)importieren Sie die Datei objidl.idl in Ihre IDL-Datei, und verknüpfen Sie sie zur Buildzeit mit oleaut32.lib. Dadurch können Sie die entsprechenden Hilfsroutinen verwenden.
-   Wenn Sie OLE-Datentypen (z. B. CLIPFORMAT, PUN, STGMEDIUM, ASYNC \_ STGMEDIUM) oder Systemhandles (z. B. HMETAFILE \_ PICT, HENHMETAFILE, HMETAFILE, HBITMAP, HPALETTE und FLOLOBAL) verwenden möchten, importieren Sie die Datei objidl.idl zur Buildzeit in Ihre Schnittstellendefinitionsdatei und verknüpfen sie mit ole32.lib.
-   Die folgenden OLE-Handles werden auch mit dem **\[ Wire \_ \] Marshal-Attribut** definiert, jedoch nur als Handles innerhalb eines Computers, da sie derzeit nicht in Remoteprozeduraufrufen an andere Computer verwendet werden können: HWND, HMENU, MARSHALLEL, HDC, HFONT, HICON, HBRUSH. Importieren Sie die Datei objidl.idl in Ihre IDL-Datei, und verknüpfen Sie sie zur Buildzeit mit ole32.lib, um diese Handles für die prozessübergreifende Kommunikation auf einem einzelnen Computer zu verwenden.

Weitere Informationen finden Sie unter [The wire \_ marshal Attribute](/windows/desktop/Rpc/the-wire-marshal-attribute), The type [ \_ UserSize Function](/windows/desktop/Rpc/the-type-usersize-function), The type [ \_ UserMarshal Function](/windows/desktop/Rpc/the-type-usermarshal-function), The type [ \_ UserUnmarshal Function](/windows/desktop/Rpc/the-type-userunmarshal-function), The type [ \_ UserFree Function](/windows/desktop/Rpc/the-type-userfree-function)und Targeting [Stubs for Specific 32-bit or 64-bit Platforms](targeting-stubs-for-specific-32-bit-or-64-bit-platforms.md).

 

 