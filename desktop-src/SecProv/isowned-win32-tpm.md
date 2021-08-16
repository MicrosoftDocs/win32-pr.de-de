---
description: Die IsOwned-Methode der Win32 \_ Tpm-Klasse gibt an, ob das Gerät über einen Besitzer verfügt. Dieser Wert wird von der TakeOwnership-Methode geändert.
ms.assetid: 04a9394f-98de-43e3-8a19-7a8f409823b8
title: IsOwned-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwned
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 01686f9b93e4dd952ce42b43d58aed9684457fb9dedeb524cea8859e0f44ba4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797110"
---
# <a name="isowned-method-of-the-win32_tpm-class"></a>IsOwned-Methode der Win32 \_ Tpm-Klasse

Die **IsOwned-Methode** der [**Win32 \_ Tpm-Klasse**](win32-tpm.md) gibt an, ob das Gerät über einen Besitzer verfügt. Dieser Wert wird von der [**TakeOwnership-Methode**](takeownership-win32-tpm.md) geändert.

## <a name="syntax"></a>Syntax


```mof
uint32 IsOwned(
  [out] boolean IsOwned
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsOwned* \[ out\]
</dt> <dd>

Typ: **boolescher Wert**

True **gibt an,** dass das Gerät über einen Besitzer verfügt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Alle TPM-Fehler und -Fehler, die für TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_Win32-tpm.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
