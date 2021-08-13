---
title: Enabled-Eigenschaft (Balloon-Objekt)
description: Erfahren Sie mehr über die Enabled Balloon-Objekteigenschaft. Microsoft Agent ist ab 7 Windows veraltet.
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d4eaa09e173d847e9dead1bbd559b59e2d12a2d40b5f1d1f989d3cf70263ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118752002"
---
# <a name="enabled-property-balloon-object"></a>Enabled-Eigenschaft (Balloon-Objekt)

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück, ob das Wort balloon für das angegebene Zeichen aktiviert ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Balloon.Enabled_*



| Wert     | BESCHREIBUNG              |
|-----------|--------------------------|
| **True**  | Die Sprechblase ist aktiviert.  |
| **False** | Die Sprechblase ist deaktiviert. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Enabled-Eigenschaft** gibt einen booleschen Wert zurück, der angibt, ob die Sprechblase aktiviert ist. Der Standardzustand des Wortsprechblasens wird als Teil der Definition eines Zeichens festgelegt, wenn das Zeichen im Microsoft Agent-Zeichen-Editor kompiliert wird. Wenn ein Zeichen so definiert ist, dass es das Wort Balloon nicht unterstützt, ist diese Eigenschaft für das Zeichen **immer** FALSE.

 

 




