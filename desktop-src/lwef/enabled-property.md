---
title: Enabled-Eigenschaft (Balloon-Objekt)
description: Erfahren Sie mehr über die Enabled Balloon-Objekteigenschaft. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602d39a9bef7713a92707d8a43050f04a3577b6d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407303"
---
# <a name="enabled-property-balloon-object"></a>Enabled-Eigenschaft (Balloon-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück, ob die Wortsprechblase für das angegebene Zeichen aktiviert ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Balloon.Enabled_*



| Wert     | BESCHREIBUNG              |
|-----------|--------------------------|
| **True**  | Die Sprechblase ist aktiviert.  |
| **False** | Die Sprechblase ist deaktiviert. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Enabled-Eigenschaft** gibt einen booleschen Wert zurück, der angibt, ob die Sprechblase aktiviert ist. Der Standardzustand des Sprechblasens wird als Teil der Definition eines Zeichens festgelegt, wenn das Zeichen im Microsoft-Agent-Zeichen-Editor kompiliert wird. Wenn ein Zeichen so definiert ist, dass es die Wortsprechblase nicht unterstützt, ist diese Eigenschaft für das Zeichen immer **False.**

 

 




