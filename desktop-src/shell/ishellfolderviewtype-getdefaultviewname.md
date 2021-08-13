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
ms.openlocfilehash: 252616bd2391606b9942777caf07a2f5f58627a316f51e481c19fbfcc98599b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443270"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a>IShellFolderViewType::GetDefaultViewName-Methode

Ruft den Namen der Standardansicht ab. Rufen [**Sie GetDisplayNameOf auf,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) um die Namen der anderen Ansichten abzurufen.

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

Die Adresse eines Zeichenfolgenzeigers, der den Standardansichtsnamen empfängt. Der Arbeitsspeicher für die Zeichenfolge wird mit [**SHStrDup zugeordnet.**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




