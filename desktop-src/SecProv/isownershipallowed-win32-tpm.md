---
description: Die IsOwnershipAllowed-Methode der Win32 \_ Tpm-Klasse gibt an, ob die Möglichkeit zum Installieren eines Besitzers für das Gerät zulässig ist.
ms.assetid: dfeb5afe-4169-470b-b5e4-cf1e5781271e
title: IsOwnershipAllowed-Methode der Win32_Tpm-Klasse
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
ms.openlocfilehash: 81363f03280d7805ce965106c7af9f1b288ae75fd9217c4af85dd80f34973a7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739550"
---
# <a name="isownershipallowed-method-of-the-win32_tpm-class"></a>IsOwnershipAllowed-Methode der Win32 \_ Tpm-Klasse

Die **IsOwnershipAllowed-Methode** der [**Win32 \_ Tpm-Klasse**](win32-tpm.md) gibt an, ob die Möglichkeit zum Installieren eines Besitzers für das Gerät zulässig ist.

## <a name="syntax"></a>Syntax


```mof
uint32 IsOwnershipAllowed(
  [out] boolean IsOwnershipAllowed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsOwnershipAllowed* \[ out\]
</dt> <dd>

Typ: **boolescher Wert**

True gibt an, dass die Möglichkeit zum Installieren eines Besitzers für das Gerät zulässig ist. False gibt an, dass die [**TakeOwnership-Methode**](takeownership-win32-tpm.md) einen Besitzer für das Gerät nicht installieren kann.

Dieser Wert kann mit der [**SetPhysicalPresenceRequest-Methode**](setphysicalpresencerequest-win32-tpm.md) geändert werden. Der Wert wird auf **TRUE** zurückgesetzt, nachdem die [**Clear-Methode**](clear-win32-tpm.md) ausgeführt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Alle TPM-Fehler sowie Fehler, die spezifisch für TPM-Basisdienste sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | Beschreibung                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
