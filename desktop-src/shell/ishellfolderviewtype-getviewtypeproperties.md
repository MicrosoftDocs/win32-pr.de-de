---
description: Ruft die Eigenschaften der Ansicht ab.
title: IShellFolderViewType::GetViewTypeProperties-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetViewTypeProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 82be6bd5-a46c-48b3-a1f0-a92b9454c35e
ms.openlocfilehash: 57e053321bbd17c90fbe82832cdb01e9acb6994438d22cb72ef62bf1e7143dd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220308"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a>IShellFolderViewType::GetViewTypeProperties-Methode

Ruft die Eigenschaften der Ansicht ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pidl* \[ In\]
</dt> <dd>

Typ: **PCUITEMID \_ CHILD**

EINE PIDL.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

Typ: **DWORD \***

Ein Zeiger auf eine Ganzzahlvariable ohne Vorzeichen, die die Ansichtseigenschaften empfängt, die angeben, was bei Auswahl der Ansicht zu tun ist. Flags können eine beliebige Kombination der folgenden Werte sein.

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG \_ NOTIFY \_ CREATE** (0x00000001)


</dt> <dd>

Erstellen Sie ein Ansichtselement, falls es nicht dort ist.

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFY \_ RESORT** (0x00000002)


</dt> <dd>

Erneutes Einreihen von PIDL und neu sortieren.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




