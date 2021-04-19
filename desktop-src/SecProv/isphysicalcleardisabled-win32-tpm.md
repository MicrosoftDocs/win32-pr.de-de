---
description: Die isphysicalcleardeaktiviert-Methode der Win32- \_ TPM-Klasse gibt an, ob nur der Gerätebesitzer das Gerät löschen kann.
ms.assetid: b87f1c4f-8735-45c5-9256-53dbb9579f95
title: Isphysicalcleardeaktiviert-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 9179aae2f4902ce29e2bab98b4c9c0b793804de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356919"
---
# <a name="isphysicalcleardisabled-method-of-the-win32_tpm-class"></a>Isphysicalcleardeaktiviert-Methode der Win32- \_ TPM-Klasse

Die **isphysicalcleardeaktiviert** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse gibt an, ob nur der Gerätebesitzer das Gerät löschen kann.

## <a name="syntax"></a>Syntax


```mof
uint32 IsPhysicalClearDisabled(
  [out] boolean IsPhysicalClearDisabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Isphysicalcleardeaktiviert* \[ vorgenommen\]
</dt> <dd>

Typ: **booleschen**

Wenn der Wert **true** ist, kann nur der Gerätebesitzer das Gerät löschen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieser Wert wird am Anfang jedes Start Zyklen auf **false** zurückgesetzt.

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

 

 
