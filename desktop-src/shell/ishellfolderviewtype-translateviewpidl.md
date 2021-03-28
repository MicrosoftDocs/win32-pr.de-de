---
description: Rekonstruiert einen Zeiger auf eine Element Bezeichner-Liste (PIDL) aus einer hierarchischen Darstellung des shellordners in eine andere Darstellung.
title: 'Ishellfolderviewtype:: translateviewpidl-Methode'
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
ms.openlocfilehash: 75876e5088c610c1f9f02ba9374db5cea4a6023c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527311"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a>Ishellfolderviewtype:: translateviewpidl-Methode

Rekonstruiert einen Zeiger auf eine Element Bezeichner-Liste (PIDL) aus einer hierarchischen Darstellung des shellordners in eine andere Darstellung.

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

*PIDL* \[ in\]
</dt> <dd>

Type: **pcuidlist \_ relative**

Das Array von Element-IDs relativ zum Stamm Ordner.

</dd> <dt>

*pidlview* \[ in\]
</dt> <dd>

Type: **pcuidlist \_ relative**

Besondere PIDL der Ansicht.

</dd> <dt>

*ppidlout* \[ in\]
</dt> <dd>

Typ: **pcuidlist \_ relative \** _

Die Adresse einer PIDL-Variablen, die die Übersetzung empfangen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn Sie fertig sind, sollten Sie die zurückgegebene PIDL mit [**ilfree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree)freigeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




