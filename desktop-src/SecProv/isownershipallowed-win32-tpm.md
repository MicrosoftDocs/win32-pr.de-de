---
description: Die isownershipallowed-Methode der Win32- \_ TPM-Klasse gibt an, ob die Möglichkeit zum Installieren eines Besitzers für das Gerät zulässig ist.
ms.assetid: dfeb5afe-4169-470b-b5e4-cf1e5781271e
title: Isownershipallowed-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnershipAllowed
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c818d5a4e4eb16ac637372f0c7ed0f2e9211ef88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214511"
---
# <a name="isownershipallowed-method-of-the-win32_tpm-class"></a>Isownershipallowed-Methode der Win32- \_ TPM-Klasse

Die **isownershipallowed** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse gibt an, ob die Möglichkeit zum Installieren eines Besitzers für das Gerät zulässig ist.

## <a name="syntax"></a>Syntax


```mof
uint32 IsOwnershipAllowed(
  [out] boolean IsOwnershipAllowed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Isownershipallowed* \[ vorgenommen\]
</dt> <dd>

Typ: **booleschen**

**True** gibt an, dass die Möglichkeit zum Installieren eines Besitzers für das Gerät zulässig ist. Wenn der Wert **false** ist, kann die Methode " [**Take Ownership**](takeownership-win32-tpm.md) " keinen Besitzer für das Gerät installieren.

Dieser Wert kann mit der [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode geändert werden. Der Wert wird nach dem Ausführen der [**Clear**](clear-win32-tpm.md) -Methode auf **true** zurückgesetzt.

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

 

 
