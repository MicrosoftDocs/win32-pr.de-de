---
description: Ruft einen Enumerator ab, der für jede erweiterte Ansicht einen Zeiger auf eine Element Bezeichner Liste (PIDL) zurückgibt.
title: 'Ishellfolderviewtype:: enumviews-Methode'
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
ms.openlocfilehash: 4ccaac7baf99608e097b8f8b67c8eac30f60ed3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993823"
---
# <a name="ishellfolderviewtypeenumviews-method"></a>Ishellfolderviewtype:: enumviews-Methode

Ruft einen Enumerator ab, der für jede erweiterte Ansicht einen Zeiger auf eine Element Bezeichner Liste (PIDL) zurückgibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*grfFlags* \[ in\]
</dt> <dd>

Typ: **ulong**

Flags, die angeben, welche Elemente in die-Enumeration eingeschlossen werden sollen. Eine Liste möglicher Werte finden Sie unter dem Enumerationstyp " [**shcontf**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) ". Dieser Parameter kann ignoriert werden.

</dd> <dt>

*ppum* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ienumittellist**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***

Die Adresse einer Zeiger Variablen vom Typ [**ienumittellist**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) , die den Enumerator empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Sichten werden dem Benutzer als ausgeblendete Ordner aus dem Stammverzeichnis (dargestellt durch pidls) dargestellt. Wenn dies erforderlich ist, wird die Standardansicht (aus dem Stamm Ordner) als **null**-oder leere PIDL dargestellt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




