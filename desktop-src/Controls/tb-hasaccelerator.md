---
title: TB_HASACCELERATOR Meldung (kommstrg. h)
description: Ruft die Anzahl der Symbolleisten Schaltflächen ab, die über das angegebene Zugriffstasten Zeichen verfügen.
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- Windows-Steuerelemente für TB_HASACCELERATOR Meldung
topic_type:
- apiref
api_name:
- TB_HASACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2544eae629876e4527ea4e47477b50ea59b796c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477103"
---
# <a name="tb_hasaccelerator-message"></a>TB- \_ hasaccelerator-Meldung

\[Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen. Diese Meldung wird möglicherweise in zukünftigen Versionen von Windows nicht mehr unterstützt.\]

Ruft die Anzahl der Symbolleisten Schaltflächen ab, die über das angegebene Zugriffstasten Zeichen verfügen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **WCHAR** , das das zu überprüfende Eingabe Beschleunigungs Zeichen darstellt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf einen **int** -Wert, der die Anzahl der Schaltflächen mit dem Zugriffstasten-Zeichen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Die Verwendung dieser Nachricht kann die Sicherheit des Programms beeinträchtigen.

## <a name="remarks"></a>Bemerkungen

Zuerst fragt das System alle Symbolleisten Schaltflächen für übereinstimmende Acceleratoren ab. Wenn keine Übereinstimmungen gefunden werden, sendet das System die [TBN \_ mapaccelerator](tbn-mapaccelerator.md) -Benachrichtigung an das übergeordnete Fenster und fordert den Index der Schaltfläche an, die über das angegebene Zugriffstasten Zeichen verfügt. Wenn das übergeordnete Element einen Index bereitstellt, wird die Anzahl auf 1 festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





