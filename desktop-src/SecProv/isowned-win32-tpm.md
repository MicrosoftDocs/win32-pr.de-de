---
description: Die isowned-Methode der Win32- \_ TPM-Klasse gibt an, ob das Gerät über einen Besitzer verfügt. Dieser Wert wird von der TakeOwnership-Methode geändert.
ms.assetid: 04a9394f-98de-43e3-8a19-7a8f409823b8
title: Isowned-Methode der Win32_Tpm-Klasse
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
ms.openlocfilehash: 6ad2d7d03059d8f96fe726d50ea18c2a70db64f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525676"
---
# <a name="isowned-method-of-the-win32_tpm-class"></a>Isowned-Methode der Win32- \_ TPM-Klasse

Die **isowned** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse gibt an, ob das Gerät über einen Besitzer verfügt. Dieser Wert wird von der [**TakeOwnership**](takeownership-win32-tpm.md) -Methode geändert.

## <a name="syntax"></a>Syntax


```mof
uint32 IsOwned(
  [out] boolean IsOwned
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Isowned* \[ vorgenommen\]
</dt> <dd>

Typ: **booleschen**

**True** gibt an, dass das Gerät über einen Besitzer verfügt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security- \\ mikrosofttpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32- \_ TPM. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32- \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ TPM**](win32-tpm.md)
</dt> </dl>

 

 
