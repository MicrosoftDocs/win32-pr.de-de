---
title: Hasotherclients (Eigenschaft)
description: Hasotherclients (Eigenschaft)
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3434cec191d2bec93d501847df064a8dbbf3e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036992"
---
# <a name="hasotherclients-property"></a>Hasotherclients (Eigenschaft)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück, ob das angegebene Zeichen von anderen Anwendungen verwendet wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent*. **Zeichen ("***Merkmal-ID***"). Hasotherclients**



| Wert     | BESCHREIBUNG                                |
|-----------|--------------------------------------------|
| **True**  | Das Zeichen hat andere Clients.           |
| **False** | Das Zeichen weist keine anderen Clients auf. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können diese Eigenschaft verwenden, um zu bestimmen, ob Ihre Anwendung der einzige oder letzte Client des Zeichens ist, wenn mehr als eine Anwendung das gleiche Zeichen gemeinsam nutzt (hat geladen).

 

 




