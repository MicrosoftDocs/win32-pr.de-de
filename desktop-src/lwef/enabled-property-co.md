---
title: Enabled-Eigenschaft (Command-Objekt)
description: Erfahren Sie mehr über die Enabled Command-Objekteigenschaft. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc0c65d5cfa0438fe9d61eac0c59e916731e057
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407333"
---
# <a name="enabled-property-command-object"></a>Enabled-Eigenschaft (Command-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück oder legt fest, ob der **Befehl** im Popupmenü des angegebenen Zeichens aktiviert ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Commands("_*_name_*_")._ *  \[  =  *Boolescher Wert* aktiviert\]



| Teil      | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der angibt, ob der **Befehl** aktiviert ist.<br/> <dl> <dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt> <dd> Der **Befehl** ist aktiviert.<br/> </dd> <dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**FALSE**</dt> <dd> Der **Befehl** ist deaktiviert.<br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn die [**Enabled-Eigenschaft**](enabled-property.md) auf **True** festgelegt ist, wird die Beschriftung der [**Command-Objekte**](/windows/desktop/lwef/the-command-object) als normaler Text im Popupmenü des Zeichens angezeigt, wenn die Clientanwendung eingabeaktiv ist. Wenn die **Enabled-Eigenschaft** **False** lautet, wird die Beschriftung als nicht verfügbarer (deaktivierter) Text angezeigt. Auf einen deaktivierten **Befehl** kann auch für die Spracheingabe nicht zugegriffen werden.

 

