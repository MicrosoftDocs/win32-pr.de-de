---
description: Deaktiviert Funktionen.
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: psetupsetglobalflags-Funktion
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
ms.openlocfilehash: 6fcb56f26d5aea233156e0fe3dfab13099d29df7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370799"
---
# <a name="psetupsetglobalflags-function"></a>psetupsetglobalflags-Funktion

\[Diese Funktion ist in Windows Vista oder Windows Server 2008 nicht verfügbar.\]

Deaktiviert Funktionen.

## <a name="syntax"></a>Syntax


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ in\]
</dt> <dd>

Die Flags, mit denen die Benutzeroberfläche oder die automatische Sicherung deaktiviert wird.



| Wert                                                                                                                                                                                                                                         | Bedeutung                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <dt>**Pspgf \_ Nicht interaktives**</dt> <dt>0x004</dt> </dl> | Legen Sie zum Deaktivieren der Benutzeroberfläche fest.<br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <dt>**Pspgf \_ Keine \_ Sicherung**</dt> <dt>0x002</dt> </dl>               | Legen Sie zum Deaktivieren der automatischen Sicherung fest.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
