---
title: Aktivierte Eigenschaft (Sprechblasen Objekt)
description: Enabled-Eigenschaft
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07179390b183e98a5eaccb2dfdb4405525d7d26e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341983"
---
# <a name="enabled-property-balloon-object"></a>Aktivierte Eigenschaft (Sprechblasen Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück, ob die Word-Sprechblase für das angegebene Zeichen aktiviert ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("**_Merkmal-ID_*_"). Sprechblase. aktiviert_*



| Wert     | BESCHREIBUNG              |
|-----------|--------------------------|
| **True**  | Die Sprechblase ist aktiviert.  |
| **False** | Die Sprechblase ist deaktiviert. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **aktivierte** Eigenschaft gibt einen booleschen Wert zurück, der angibt, ob die Sprechblase aktiviert ist. Der Standardzustand der Word-Sprechblase wird als Teil der Definition eines Zeichens festgelegt, wenn das Zeichen im Microsoft-Agent-Zeichen-Editor kompiliert wird. Wenn ein Zeichen definiert ist, um die Word-Sprechblase nicht zu unterstützen, wird diese Eigenschaft für das Zeichen immer **false** sein.

 

 




