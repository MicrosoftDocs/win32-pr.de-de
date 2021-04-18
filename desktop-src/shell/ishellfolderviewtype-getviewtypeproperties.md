---
description: Ruft die Eigenschaften der Ansicht ab.
title: 'Ishellfolderviewtype:: getviewtypeproperties-Methode'
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
ms.openlocfilehash: f4368edf6eae3e6892a3d81147401e061548f6e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977928"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a>Ishellfolderviewtype:: getviewtypeproperties-Methode

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

*PIDL* \[ in\]
</dt> <dd>

Type: **pcuitemid \_ Child**

eine PIDL.

</dd> <dt>

*pdwflags* \[ vorgenommen\]
</dt> <dd>

Typ: **DWORD \** _

Ein Zeiger auf eine ganzzahlige Variable ohne Vorzeichen, die die Ansichts Eigenschaften empfängt und angibt, was beim Auswählen der Sicht geschehen soll. Flags können eine beliebige Kombination der folgenden Werte sein.

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *Sfvtflag \_ Notify \_ Create** (0x00000001)


</dt> <dd>

Erstellen Sie ein Ansichts Element, wenn nicht vorhanden.

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**Sfvtflag \_ \_Ressort Benachrichtigen** (0x00000002)


</dt> <dd>

Resert PIDL und resortieren.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




