---
description: Deaktiviert Features.
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: pSetupSetGlobalFlags-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupSetGlobalFlags
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: d28bb948d351b2b9ad54c7e2bdc8c8cbfde83f6f4ade42a0f90440eca28bfc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955699"
---
# <a name="psetupsetglobalflags-function"></a>pSetupSetGlobalFlags-Funktion

\[Diese Funktion ist in Windows Vista oder Windows Server 2008 nicht verfügbar.\]

Deaktiviert Features.

## <a name="syntax"></a>Syntax


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ In\]
</dt> <dd>

Die Flags, die zum Deaktivieren der Benutzeroberfläche oder der automatischen Sicherung verwendet werden.



| Wert                                                                                                                                                                                                                                         | Bedeutung                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <dt>**PSPGF \_ NONINTERACTIVE-0x004**</dt> <dt></dt> </dl> | Legen Sie diese Einstellung fest, um die Benutzeroberfläche zu deaktivieren.<br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <dt>**PSPGF \_ NO \_ BACKUP**</dt> <dt>0x002</dt> </dl>               | Legen Sie diese Einstellung fest, um die automatische Sicherung zu deaktivieren.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
