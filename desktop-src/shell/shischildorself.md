---
UID: ''
title: SHIsChildOrSelf-Funktion
description: Vergleicht, ob ein Fenster gleich , ein untergeordnetes Element von oder ein Nachfolger von einem zweiten Fenster ist.
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
ms.openlocfilehash: f2d8eaab0f17647a6f548a0243199073baef074c88dad6a3f7100cfbca1a02be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941330"
---
# <a name="shischildorself-function"></a>SHIsChildOrSelf-Funktion

## <a name="description"></a>BESCHREIBUNG

\[Diese Funktion ist über Windows XP und Windows Server 2003 verfügbar.
Sie kann in nachfolgenden Versionen von geändert oder nicht verfügbar Windows.\]

Vergleicht, ob ein Fenster gleich , ein untergeordnetes Element von oder ein Nachfolger von einem zweiten Fenster ist.

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

### <a name="hwnd-in"></a>hwnd [in]

Typ: **HWND**

Ein Handle für ein Fenster, das mit *hwndParent getestet werden soll.*

## <a name="returns"></a>Gibt zurück

Typ: **HRESULT**

Gibt **S_OK** zurück, wenn das von *hwnd* angegebene Fenster gleich oder ein untergeordnetes Fenster von oder ein untergeordnetes Fenster ist, das von *hwndParent angegeben wird.*
Gibt **S_FALSE** zurück, wenn das von hwnd angegebene Fenster nicht gleich, kein untergeordnetes Fenster von und kein absteigender Teil des durch *hwndParent* angegebenen Fensters ist.
Der Rückgabewert ist nicht definiert, wenn ein Fensterhand handle ungültig ist.

## <a name="remarks"></a>Hinweise

## <a name="see-also"></a>Siehe auch

[IsChild](/windows/desktop/api/winuser/nf-winuser-ischild)
