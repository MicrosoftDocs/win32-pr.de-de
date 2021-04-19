---
UID: ''
title: Guardchecklongjumptarget-Funktion
description: Versucht, zu überprüfen, ob das Ziel eines longjmp gültig ist.
old-location: ''
ms.assetid: na
ms.date: 04/02/2019
ms.keywords: ''
ms.topic: reference
req.header: guardapiset.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- api-ms-win-core-guard-l1-1-0.dll
api_name:
- GuardCheckLongJumpTarget
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 02f659f77ab2bace129c9b9d9011b4c93e59b2f4
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2020
ms.locfileid: "106338653"
---
# <a name="guardchecklongjumptarget-function"></a>Guardchecklongjumptarget-Funktion

## <a name="description"></a>BESCHREIBUNG

Versucht, zu überprüfen, ob das Ziel eines [longjmp](/cpp/c-runtime-library/reference/longjmp) für einen Prozess gültig ist, für den [Control Flow Guard (CFG)](../secbp/control-flow-guard.md) aktiviert ist.

Wenn die Zieladresse einer Bild Zuordnung entspricht, werden die gültigen Ziele für die Binärdatei extrahiert.
Die-Funktion verwendet diese Ziele, um das Ziel zu validieren.
Wenn die Binärdatei keine Metadaten enthält, mit denen der Satz gültiger *longjmp* -Ziele beschrieben wird, gibt die Funktion **true** zurück.

Wenn die Zieladresse einer Zuordnung ohne Image entspricht, wie in JIT-Code, wird eine globale schreibgeschützte Richtlinie mit einer globalen schreibgeschützten Richtlinie abgefragt, um zu bestimmen, ob der Sprung zulässig ist.

## <a name="parameters"></a>Parameter

### <a name="targetaddress-in"></a>TargetAddress [in]

Die Zieladresse für den Sprung.

### <a name="flags-in"></a>Flags [in]

Flags, die den Vorgang beschreiben, der für die Adresse ausgeführt werden soll.
Wenn Sie **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1) angeben, beendet diese Funktion den Prozess nicht, wenn das Ziel ungültig ist.

## <a name="returns"></a>Gibt zurück

**True** , wenn das Ziel gültig ist, andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

## <a name="see-also"></a>Siehe auch
