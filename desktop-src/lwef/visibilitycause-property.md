---
title: VisibilityCause-Eigenschaft
description: VisibilityCause-Eigenschaft
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1e90b77dfdfae364761254676d0867a43aebacf516d4f2adad2973700d7e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398790"
---
# <a name="visibilitycause-property"></a>VisibilityCause-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen ganzzahligen Wert zurück, der angibt, was den sichtbaren Zustand des Zeichens verursacht hat.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent .* **Characters("**_CharacterID_*_"). VisibilityCause_*



| Wert | Beschreibung                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| 0     | Das Zeichen wurde nicht angezeigt.                                                                            |
| 1     | Der Benutzer hat das Zeichen mithilfe des Befehls im Popupmenü des Taskleistensymbols des Zeichens oder mithilfe der Spracheingabe ausgeblendet. |
| 2     | Der Benutzer hat das Zeichen gezeigt.                                                                               |
| 3     | Ihre Anwendung hat das Zeichen ausgeblendet.                                                                          |
| 4     | Ihre Anwendung hat das Zeichen angezeigt.                                                                       |
| 5     | Eine andere Clientanwendung hat das Zeichen ausgeblendet.                                                                |
| 6     | Eine andere Clientanwendung hat das Zeichen gezeigt.                                                             |
| 7     | Der Benutzer hat das Zeichen mithilfe des Befehls im Popupmenü des Zeichens ausgeblendet.                                 |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können diese Eigenschaft verwenden, um zu bestimmen, wodurch das Zeichen verschoben wurde, wenn mehrere Anwendungen das gleiche Zeichen gemeinsam nutzen (geladen haben). Diese Werte sind identisch mit denen, [**die**](show-event.md) von den Show- und [**Hide-Ereignissen**](hide-event.md) zurückgegeben werden.

## <a name="see-also"></a>Weitere Informationen

[**Ereignis ausblenden,**](hide-event.md) [**Ereignis anzeigen,**](show-event.md) [**Methode ausblenden,**](hide-method.md) [**Methode anzeigen**](show-method.md)


 

 




