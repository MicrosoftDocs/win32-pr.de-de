---
description: 'pSetupStringTableInitializeEx-Funktion: Initialisiert eine Zeichenfolgentabelle.'
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: pSetupStringTableInitializeEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 189bb94b70366ad66f0fe4dd4c4c9d5884e762cf20638f7c3ae2dc9b587f15ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538470"
---
# <a name="psetupstringtableinitializeex-function"></a>pSetupStringTableInitializeEx-Funktion

\[Diese Funktion ist in Windows Vista oder Windows Server 2008 nicht verfügbar.\]

Initialisiert eine Zeichenfolgentabelle.

## <a name="syntax"></a>Syntax


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ExtraDataSize* \[ In\]
</dt> <dd>

Größe des zusätzlichen Datenobjekts.

</dd> <dt>

*Reserviert* \[ In\]
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
