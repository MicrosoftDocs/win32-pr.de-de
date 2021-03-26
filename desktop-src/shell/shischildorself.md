---
UID: ''
title: Shischildorself-Funktion
description: Vergleicht, ob ein Fenster gleich, ein untergeordnetes Element von oder ein Nachfolger von, einem zweiten Fenster ist.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: IsChild
ms.topic: reference
req.header: Shlwapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
- SHIsChildOrSelf
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 911bb0b2a544197ca6db761e05adac79e97c3f69
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "104993303"
---
# <a name="shischildorself-function"></a>Shischildorself-Funktion

## <a name="description"></a>BESCHREIBUNG

\[Diese Funktion ist über Windows XP und Windows Server 2003 verfügbar.
Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]

Vergleicht, ob ein Fenster gleich, ein untergeordnetes Element von oder ein Nachfolger von, einem zweiten Fenster ist.

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a>Parameter

### <a name="hwndparent-in"></a>hwndParent [in]

Typ: **HWND**

Ein Handle für das erste Fenster.

### <a name="hwnd-in"></a>HWND [in]

Typ: **HWND**

Ein Handle für ein Fenster, das auf *hwndParent* getestet werden soll.

## <a name="returns"></a>Gibt zurück

Typ: **HRESULT**

Gibt **S_OK** zurück, wenn das von *HWND* angegebene Fenster gleich, ein untergeordnetes Element von oder ein Nachfolger des Fensters ist, das von *hwndParent* angegeben wird.
Gibt **S_FALSE** zurück, wenn das von HWND angegebene Fenster nicht gleich und kein untergeordnetes Element von ist und kein Nachfolger des Fensters ist, das von *hwndParent* angegeben wird.
Der Rückgabewert ist nicht definiert, wenn ein Fenster Handle ungültig ist.

## <a name="remarks"></a>Bemerkungen

## <a name="see-also"></a>Weitere Informationen

[IsChild](/windows/desktop/api/winuser/nf-winuser-ischild)
