---
title: "\"Settings. Volume\""
description: Die Volume-Eigenschaft gibt das aktuelle Volume an oder ruft es ab.
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- Windows-Media Player "Settings. Volume"
topic_type:
- apiref
api_name:
- Settings.volume
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f5ec4299bf33ed16143eec8570b65c548599e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369666"
---
# <a name="settingsvolume"></a>"Settings. Volume"

Die **Volume** -Eigenschaft gibt das aktuelle Volume an oder ruft es ab.

## <a name="syntax"></a>Syntax

Player. Settings. Volume

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/schreibzahl (**Long**) im Bereich von 0 bis 100. 

## <a name="remarks"></a>Bemerkungen

NULL gibt kein Volume an, und 100 gibt das vollständige Volume an. Wenn für diese Eigenschaft kein Wert angegeben wird, wird standardmäßig die letzte für den Player festgelegte volumeeinstellung verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Einstellungs Objekt**](settings-object.md)
</dt> </dl>

 

 





