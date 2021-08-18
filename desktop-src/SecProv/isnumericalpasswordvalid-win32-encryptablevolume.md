---
description: Gibt an, ob das numerische Kennwort die speziellen Formatanforderungen für diesen Authentifizierungswert erfüllt.
ms.assetid: 3995405f-db4d-4f72-98dc-133a09f9cf65
title: IsNumericalPasswordValid-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsNumericalPasswordValid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0aed00554d7a8e284f83659dc92266b1ce5e098f1b102e6444bfc07fd2909066
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739640"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a>IsNumericalPasswordValid-Methode der Win32 \_ EncryptableVolume-Klasse

Die **IsNumericalPasswordValid-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) gibt an, ob das numerische Kennwort die speziellen Formatanforderungen für diesen Authentifizierungswert erfüllt.

## <a name="syntax"></a>Syntax


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NumericalPassword* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die das numerische Kennwort angibt.

Das numerische Kennwort muss 48 Ziffern enthalten. Diese Ziffern können in acht Gruppen von 6 Ziffern unterteilt werden, wobei die letzte Ziffer in jeder Gruppe einen Prüfsummenwert für die Gruppe angibt. Jede Gruppe von 6 Ziffern muss durch 11 teilbar sein und kleiner als 720896 sein. Wenn eine Gruppe von sechs Ziffern als x1, x2, x3, x4, x5 und x6 bezeichnet wird, wird die x6-Prüfsummenziffer als –x1+x2–x3+x4–x5 mod 11 berechnet.

Die Zifferngruppen können optional durch ein Leerzeichen oder einen Bindestrich getrennt werden. Daher können "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" oder "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" auch gültige numerische Kennwörter enthalten.

</dd> <dt>

*IsNumericalPasswordValid* \[ out\]
</dt> <dd>

Typ: **boolescher Wert**

Ein boolescher Wert, der true ist, wenn das numerische Kennwort die speziellen Formatanforderungen für diesen Authentifizierungswert erfüllt, andernfalls false.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.



| Rückgabecode/-wert                                                                                                                                 | Beschreibung                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, nur Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CIMV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
