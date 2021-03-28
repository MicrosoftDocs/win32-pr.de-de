---
description: Öffnet ein angegebenes Volume und initialisiert dessen Kontingent Steuerungsobjekt.
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: DiskQuotaControl.Initialize-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.Initialize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 919720f01c67b6df3189b760aa8cefbb29615179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977176"
---
# <a name="diskquotacontrolinitialize-method"></a>DiskQuotaControl.Initialize-Methode

Öffnet ein angegebenes Volume und initialisiert dessen Kontingent Steuerungsobjekt.

## <a name="syntax"></a>Syntax


```JScript
DiskQuotaControl.Initialize(
  sPath,
  bReadWrite
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Spath* 
</dt> <dd>

Typ: **Zeichenfolge**

Ein Zeichen folgen Wert, der den voll qualifizierten Pfad des zu initialisierenden Volumes enthält.

</dd> <dt>

*breadwrite* 
</dt> <dd>

Typ: **Boolean**

Ein boolescher Wert, der angibt, wie das Volume geöffnet werden soll. Legen Sie *breadwrite* für Lese-/Schreibzugriff auf " **true** " oder " **false** " für schreibgeschützten Zugriff fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Diskquotacontrol-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




