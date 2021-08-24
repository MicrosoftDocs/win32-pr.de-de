---
title: TB_HASACCELERATOR Meldung (Commctrl.h)
description: Ruft die Anzahl der Symbolleistenschaltflächen ab, die das angegebene Zugriffstastenzeichen aufweisen.
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- TB_HASACCELERATOR Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 420f06e71c6920c266c96d8b2580549fa0eaace2bd3abdd37524502d4039aa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078284"
---
# <a name="tb_hasaccelerator-message"></a>\_TB-HASACCELERATOR-Nachricht

\[Für die interne Verwendung vorgesehen; nicht für die Verwendung in Anwendungen empfohlen. Diese Meldung wird in zukünftigen Versionen von Windows möglicherweise nicht mehr unterstützt.\]

Ruft die Anzahl der Symbolleistenschaltflächen ab, die das angegebene Zugriffstastenzeichen aufweisen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **WCHAR,** der das zu testde eingabetastenzeichen darstellt.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Wert vom Typ int, der die Anzahl der Schaltflächen mit dem Zugriffstastenzeichen **empfängt.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Die Verwendung dieser Meldung kann die Sicherheit Ihres Programms gefährden.

## <a name="remarks"></a>Hinweise

Zunächst fragt das System alle Symbolleistenschaltflächen nach übereinstimmenden Zugriffstasten ab. Wenn keine Übereinstimmungen gefunden werden, sendet das System die [ \_ TBN-MAPACCELERATOR-Benachrichtigung](tbn-mapaccelerator.md) an das übergeordnete Fenster und fordert den Index der Schaltfläche mit dem angegebenen Zugriffstastenzeichen an. Wenn das übergeordnete Element einen Index bereitstellt, wird die Anzahl auf 1 festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





