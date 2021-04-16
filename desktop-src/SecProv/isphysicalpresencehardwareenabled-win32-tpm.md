---
description: Die isphysicalpresencehardwareaktivierte-Methode der Win32 \_ TPM-Klasse gibt an, ob die physische Präsenz auf der Plattform mit einem Hardware Signal festgelegt werden kann.
ms.assetid: 65dabfa9-bfbe-4b9b-8e80-02269895c7ad
title: Isphysicalpresencehardwareaktivierte Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalPresenceHardwareEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 674dcaa733d8ec70af172359e3dcde0578955dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393493"
---
# <a name="isphysicalpresencehardwareenabled-method-of-the-win32_tpm-class"></a>Isphysicalpresencehardwareaktivierte Methode der Win32- \_ TPM-Klasse

Die **isphysicalpresencehardwareaktivierte** -Methode der [**Win32 \_ TPM**](win32-tpm.md) -Klasse gibt an, ob die physische Präsenz auf der Plattform mit einem Hardware Signal festgelegt werden kann. Dieser Wert wird vom Platt Form Hersteller basierend auf dem Entwurf der Plattform konfiguriert. Die Dokumentation des Platt Form Herstellers bietet möglicherweise weitere Informationen.

## <a name="syntax"></a>Syntax


```mof
uint32 IsPhysicalPresenceHardwareEnabled(
  [out] boolean IsPhysicalPresenceHardwareEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Isphysicalpresencehardwareaktivierte* \[ vorgenommen\]
</dt> <dd>

Typ: **booleschen**

**True** gibt an, dass die physische Präsenz auf der Plattform mit einem Hardware Signal festgelegt werden kann.

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

 

 
