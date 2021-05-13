---
description: Ruft einen Enumerator ab, der einen Zeiger auf eine Elementbezeichnerliste (PIDL) für jede erweiterte Ansicht zurückgibt.
title: IShellFolderViewType::EnumViews-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.EnumViews
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e44cd774-1d16-4faa-b5ca-fcaf2740cdca
ms.openlocfilehash: 1627bb134066821444788ca44a3527278a02f4c7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842771"
---
# <a name="ishellfolderviewtypeenumviews-method"></a>IShellFolderViewType::EnumViews-Methode

Ruft einen Enumerator ab, der einen Zeiger auf eine Elementbezeichnerliste (PIDL) für jede erweiterte Ansicht zurückgibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*grfFlags* \[ In\]
</dt> <dd>

Typ: **ULONG**

Flags, die angeben, welche Elemente in die Enumeration eingeschlossen werden sollen. Eine Liste der möglichen Werte finden Sie unter [**SHCONTF-Enumerationstyp.**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) Dieser Parameter kann ignoriert werden.

</dd> <dt>

*ppenum* \[ out\]
</dt> <dd>

Typ: **[ **IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***

Die Adresse einer Zeigervariable vom Typ [**IEnumIDList,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) die den Enumerator empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Ansichten werden dem Benutzer als ausgeblendete Ordner außerhalb des Stammverzeichnisses (dargestellt durch PIDLs) dargestellt. Bei Bedarf wird die Standardansicht (außerhalb des Stammordners) als **NULL** oder als leere PIDL dargestellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




