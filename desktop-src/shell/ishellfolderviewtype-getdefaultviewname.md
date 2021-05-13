---
description: Ruft den Namen der Standardansicht ab. Rufen Sie GetDisplayNameOf auf, um die Namen der anderen Ansichten abzurufen.
title: IShellFolderViewType::GetDefaultViewName-Methode
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
ms.openlocfilehash: 808f68093512e2da602d5e73775b47943b140a46
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842761"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a>IShellFolderViewType::GetDefaultViewName-Methode

Ruft den Namen der Standardansicht ab. Rufen [**Sie GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) auf, um die Namen der anderen Ansichten abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uFlags* \[ In\]
</dt> <dd>

Typ: **DWORD**

Optionale Flags; sollte auf 0 festgelegt werden.

</dd> <dt>

*ppwszName* \[ out\]
</dt> <dd>

Typ: **LPWSTR \***

Die Adresse eines Zeichenfolgenzeigers, der den Standardansichtsnamen empfängt. Der Arbeitsspeicher für die Zeichenfolge wird mit [**SHStrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa)zugeordnet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




