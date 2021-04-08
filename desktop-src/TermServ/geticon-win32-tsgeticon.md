---
title: GetIcon-Methode der Win32_TSGetIcon-Klasse
description: Gibt den Inhalt des angegebenen Symbols zurück.
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- GetIcon-Methode Remotedesktopdienste
- GetIcon-Methode Remotedesktopdienste, Win32_TSGetIcon-Klasse
- Win32_TSGetIcon-Klasse Remotedesktopdienste, GetIcon-Methode
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
ms.openlocfilehash: 92cd20cad668b0e3a6bba191c83ecdca2934ca17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949505"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a>GetIcon-Methode der Win32- \_ Klasse "zgeticon"

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

*FilePath* \[ in\]
</dt> <dd>

Gibt den Pfad zu der Datei an, in der das Symbol enthalten ist.

</dd> <dt>

*Index* \[ in\]
</dt> <dd>

Gibt den Index des Symbols in der Datei an.

</dd> <dt>

*Iconcontent* \[ vorgenommen\]
</dt> <dd>

Nach erfolgreichem Abschluss enthält der Inhalt des Symbols.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow. MOF</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Zeit \_ Ticon**](win32-tsgeticon.md)
</dt> </dl>

 

 





