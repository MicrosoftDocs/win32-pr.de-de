---
title: HasOtherClients-Eigenschaft
description: HasOtherClients-Eigenschaft
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7bb91240ade815c00fb2e36adf1466dcb30ba4240be038342906be49e6ff2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479005"
---
# <a name="hasotherclients-property"></a>HasOtherClients-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück, ob das angegebene Zeichen von anderen Anwendungen verwendet wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent .* **Characters("**_CharacterID_*_"). HasOtherClients_*



| Wert     | BESCHREIBUNG                                |
|-----------|--------------------------------------------|
| **True**  | Das Zeichen verfügt über andere Clients.           |
| **False** | Das Zeichen verfügt nicht über andere Clients. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können diese Eigenschaft verwenden, um zu bestimmen, ob Ihre Anwendung der einzige oder letzte Client des Zeichens ist, wenn mehr als eine Anwendung das gleiche Zeichen gemeinsam verwendet (geladen hat).

 

 




