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
ms.openlocfilehash: 78ee96e7e366fdff821e8202300ff28de0a14af3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096648"
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

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
