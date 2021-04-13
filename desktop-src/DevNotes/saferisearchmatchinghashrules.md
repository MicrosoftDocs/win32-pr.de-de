---
description: Ruft die Ebene einer Hash Identifikations Regel ab, die dem angegebenen Hash entspricht.
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: Saferisearchmatchinghashrules-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SaferiSearchMatchingHashRules
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
ms.openlocfilehash: 2d1b7a2b2ce3f0f0e45d87a46219f3ee4d999bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483646"
---
# <a name="saferisearchmatchinghashrules-function"></a>Saferisearchmatchinghashrules-Funktion

Ruft die Ebene einer Hash Identifikations Regel ab, die dem angegebenen Hash entspricht.

Diese Funktion verfügt über keine zugeordnete Import Bibliothek und ist nicht in einem öffentlichen Header deklariert. Sie müssen einen Funktionszeiger mit der Signatur dieser Funktion definieren, und Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Advapi32.dll zu verknüpfen.

Es wird empfohlen, die Funktion " [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) " zum Auswerten von Software Einschränkungs Richtlinien zu verwenden.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SaferiSearchMatchingHashRules(
  _In_opt_ ALG_ID HashAlgorithm,
  _In_     PBYTE  pHashBytes,
  _In_     DWORD  dwHashSize,
  _In_opt_ DWORD  dwOriginalImageSize,
  _Out_    PDWORD pdwFoundLevel,
           PDWORD pdwSaferFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HashAlgorithm* \[ in, optional\]
</dt> <dd>

Der Bezeichner des Algorithmus, der zum Erstellen des Hashwerts verwendet wird.

</dd> <dt>

*phashbytes* \[ in\]
</dt> <dd>

Ein Zeiger auf ein Bytearray, das den Hash enthält.

</dd> <dt>

*dwhashsize* \[ in\]
</dt> <dd>

Die Größe des *phashbytes* -Arrays in Bytes.

</dd> <dt>

*dworiginalimagesize* \[ in, optional\]
</dt> <dd>

Die Größe des ursprünglichen Bilds (in Bytes), aus dem der Hash berechnet wurde.

</dd> <dt>

*pdwfoundlevel* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den Bezeichner der Ebene für die entsprechende Hash Identifikations Regel.

</dd> <dt>

*pdwsaferflags* 
</dt> <dd>

Reserviert. Legen Sie diesen Wert auf NULL fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**True** , wenn die Funktion erfolgreich ist. andernfalls **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl> |



 

 
