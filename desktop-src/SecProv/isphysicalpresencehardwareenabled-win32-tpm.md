---
description: Die IsPhysicalPresenceHardwareEnabled-Methode der Win32 Tpm-Klasse gibt an, ob die physische Präsenz auf der Plattform mit einem \_ Hardwaresignal festgelegt werden kann.
ms.assetid: 65dabfa9-bfbe-4b9b-8e80-02269895c7ad
title: IsPhysicalPresenceHardwareEnabled-Methode der Win32_Tpm Klasse
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
ms.openlocfilehash: 499ec39741b23583b599407ef43696ab82164f365626c8042586b6b6e4b56deb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797040"
---
# <a name="isphysicalpresencehardwareenabled-method-of-the-win32_tpm-class"></a>IsPhysicalPresenceHardwareEnabled-Methode der Win32 \_ Tpm-Klasse

Die **IsPhysicalPresenceHardwareEnabled-Methode** der [**Win32 \_ Tpm-Klasse**](win32-tpm.md) gibt an, ob die physische Präsenz auf der Plattform mit einem Hardwaresignal festgelegt werden kann. Dieser Wert wird vom Plattformhersteller basierend auf dem Entwurf der Plattform konfiguriert. Die Dokumentation des Plattformherstellers enthält möglicherweise zusätzliche Informationen.

## <a name="syntax"></a>Syntax


```mof
uint32 IsPhysicalPresenceHardwareEnabled(
  [out] boolean IsPhysicalPresenceHardwareEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsPhysicalPresenceHardwareEnabled* \[ out\]
</dt> <dd>

Typ: **boolescher Wert**

True **gibt an,** dass die physische Präsenz auf der Plattform mit einem Hardwaresignal festgelegt werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Alle TPM-Fehler und -Fehler, die für TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | Beschreibung                           |
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
