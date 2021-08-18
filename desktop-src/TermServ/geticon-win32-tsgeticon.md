---
title: GetIcon-Methode der Win32_TSGetIcon-Klasse
description: Gibt den Inhalt des angegebenen Symbols zurück.
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- GetIcon-Methode Remotedesktopdienste
- GetIcon-Methode Remotedesktopdienste , Win32_TSGetIcon-Klasse
- Win32_TSGetIcon-Klasse Remotedesktopdienste , GetIcon-Methode
topic_type:
- apiref
api_name:
- Win32_TSGetIcon.GetIcon
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305316d66ce95659210396a10f22366d64ebdd2b410b056aa3c398cf65edbbf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001538"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a>GetIcon-Methode der Win32 \_ TSGetIcon-Klasse

Gibt den Inhalt des angegebenen Symbols zurück.

## <a name="syntax"></a>Syntax


```mof
uint32 GetIcon(
  [in]  string FilePath,
  [in]  sint32 Index,
  [out] uint8  IconContents[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FilePath* \[ In\]
</dt> <dd>

Gibt den Pfad zu der Datei an, die das Symbol enthält.

</dd> <dt>

*Index* \[ In\]
</dt> <dd>

Gibt den Index des Symbols in der Datei an.

</dd> <dt>

*IconContents* \[ out\]
</dt> <dd>

Enthält nach erfolgreichem Abschluss den Inhalt des Symbols.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow.mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGetIcon**](win32-tsgeticon.md)
</dt> </dl>

 

 





