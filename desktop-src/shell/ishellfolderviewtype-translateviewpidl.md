---
description: Rekonstruiert einen Zeiger auf eine Elementbezeichnerliste (PIDL) aus einer hierarchischen Darstellung des Shellordners in einer anderen Darstellung.
title: IShellFolderViewType::TranslateViewPidl-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.TranslateViewPidl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b7fa6c4-3d02-44ed-b63d-80a799e4017a
ms.openlocfilehash: 537a77e7ffffb462e0031ea0959f60cd695f7d99
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842671"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a>IShellFolderViewType::TranslateViewPidl-Methode

Rekonstruiert einen Zeiger auf eine Elementbezeichnerliste (PIDL) aus einer hierarchischen Darstellung des Shellordners in einer anderen Darstellung.

## <a name="syntax"></a>Syntax


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pidl* \[ In\]
</dt> <dd>

Typ: **PCUIDLIST \_ RELATIVE**

Das Array von Element-IDs relativ zum Stammordner.

</dd> <dt>

*pidlView* \[ In\]
</dt> <dd>

Typ: **PCUIDLIST \_ RELATIVE**

Spezielle PIDL der Ansicht.

</dd> <dt>

*dldlOut* \[ In\]
</dt> <dd>

Typ: **PCUIDLIST \_ RELATIVE \***

Die Adresse einer PIDL-Variablen, die die Übersetzung empfangen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn Sie fertig sind, sollten Sie die zurückgegebene PIDL mit [**ILFree frei geben.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




