---
description: Ruft den Namen der Standardansicht ab. Rufen Sie GetDisplayNameOf auf, um die Namen der anderen Sichten abzurufen.
title: 'Ishellfolderviewtype:: getdefaultviewname-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetDefaultViewName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 99229d13-40dc-4750-81a7-48a2f608b778
ms.openlocfilehash: 239fcd80bcfc0b29287f8e16aeef3efb8ae032c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977937"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a>Ishellfolderviewtype:: getdefaultviewname-Methode

Ruft den Namen der Standardansicht ab. Rufen Sie [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) auf, um die Namen der anderen Sichten abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uFlags* \[ in\]
</dt> <dd>

Typ: **DWORD**

Optionale Flags; muss auf 0 festgelegt werden.

</dd> <dt>

*ppwszname* \[ vorgenommen\]
</dt> <dd>

Typ: **LPWSTR \** _

Die Adresse eines Zeichen folgen Zeigers, der den Standard Ansichts Namen empfängt. Der Arbeitsspeicher für die Zeichenfolge wird mit [_ *shundup* *](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa)zugeordnet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




