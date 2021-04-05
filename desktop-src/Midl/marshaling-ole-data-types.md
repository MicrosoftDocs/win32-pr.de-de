---
title: Marshalling von OLE-Datentypen
description: Marshalling von Automatisierungs-und OLE-Datentypen.
ms.assetid: 0cab4208-d40d-40a1-88f2-4933b52c0c29
keywords:
- Mittel l und com-Mittell, Mars Hallen von OLE-Datentypen
- Marshalling von mittlerer l
- OLE-Daten-Mittelwert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5970c6e0fef9d0fc88b8a0a11a087fa4396d7a7c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725153"
---
# <a name="marshaling-ole-data-types"></a>Marshalling von OLE-Datentypen

Um die Verwendung bestimmter Automatisierungs-und OLE-Datentypen sowie einiger in com häufig verwendeter System Handles zu vereinfachen, sind Typedefs für diese Datentypen und die zugehörigen Hilfsfunktionen verfügbar, wenn Sie Windows-IDL-Dateien importieren und mit den OLE-und Automatisierungs-dll-Dateien verknüpfen. Diese Dateien werden automatisch auf Ihrem System installiert.

-   Wenn Sie den [**BSTR**](/previous-versions/windows/desktop/automat/bstr) -Datentyp in Remote Prozedur aufrufen verwenden möchten, importieren Sie die Wtypes. IDL-Datei in die IDL-Datei (Interface Definition), und verknüpfen Sie Sie mit Oleaut32. lib, wenn Sie die verteilte Anwendung aufbauen. Dies ermöglicht Ihren Stub die Verwendung der vorgefertigten Hilfsfunktionen **BSTR \_ usersize**, **BSTR \_ usermarshal**, **BSTR \_ userunmarshal** und **BSTR \_ userfree**.
-   Um andere Automatisierungs Datentypen (z. b. [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) und [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray)) oder Typen zu verwenden, die diese Typen verwenden (z. b. [**dispparameams**](/windows/win32/api/oaidl/ns-oaidl-dispparams) und [**EXCEPINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo)), importieren Sie die objidl. IDL-Datei in Ihre IDL-Datei, und verknüpfen Sie Sie zur Buildzeit mit Oleaut32. lib. Auf diese Weise können Sie die entsprechenden Hilfsroutinen verwenden.
-   Um OLE-Datentypen (z. b. clipFormat) zu verwenden, "SNB", "STGMEDIUM", "Async \_ STGMEDIUM") oder System Handles (z. b. "HMETAFILE \_ PICT", "HENHMETAFILE", "HMETAFILE", "HBITMAP", "hpalette" und "HGLOBAL") importieren Sie die Datei "objidl
-   Die folgenden OLE-Handles werden ebenfalls mit dem **\[ Wire \_ Marshal \]** -Attribut definiert, jedoch nur als Handles innerhalb eines Computers, da Sie zurzeit nicht in Remote Prozedur aufrufen an andere Computer verwendet werden können: HWND, HMENU, haccel, HDC, hFont, HICON und hBrush. Importieren Sie die objidl. IDL-Datei in Ihre IDL-Datei, und verknüpfen Sie Sie zur Buildzeit mit ole32. lib, um diese Handles bei der prozessübergreifenden Kommunikation auf einem einzelnen Computer zu verwenden.

Weitere Informationen finden Sie unter [dem Wire \_ Marshal-Attribut](/windows/desktop/Rpc/the-wire-marshal-attribute), [der Type \_ usersize-Funktion](/windows/desktop/Rpc/the-type-usersize-function), [der Type \_ usermarshal](/windows/desktop/Rpc/the-type-usermarshal-function)-Funktion, [der Type \_ userunmarshal-Funktion](/windows/desktop/Rpc/the-type-userunmarshal-function), [der Type \_ userfree-Funktion](/windows/desktop/Rpc/the-type-userfree-function)und der [Zielplattform-Stub für bestimmte 32-Bit-oder 64-Bit-Plattformen](targeting-stubs-for-specific-32-bit-or-64-bit-platforms.md).

 

 