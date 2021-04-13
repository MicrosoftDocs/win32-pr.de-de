---
title: Visibilitycause (Eigenschaft)
description: Visibilitycause (Eigenschaft)
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6e21e2cda201f8d04837d2b10efc757b93f824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388345"
---
# <a name="visibilitycause-property"></a>Visibilitycause (Eigenschaft)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen ganzzahligen Wert zurück, der angibt, wodurch der sichtbare Zustand des Zeichens verursacht wurde.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent*. **Zeichen ("***Merkmal-ID***"). Visibilitycause**



| Wert | BESCHREIBUNG                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| 0     | Das Zeichen wurde nicht angezeigt.                                                                            |
| 1     | Der Benutzer hat das Zeichen mit dem Befehl im Popup Menü des Task leisten Symbols des Zeichens oder mithilfe der Spracheingabe ausgeblendet. |
| 2     | Der Benutzer hat das Zeichen angezeigt.                                                                               |
| 3     | Die Anwendung hat das Zeichen verborgen.                                                                          |
| 4     | Die Anwendung hat das Zeichen angezeigt.                                                                       |
| 5     | Eine andere Client Anwendung hat das Zeichen verborgen.                                                                |
| 6     | Das Zeichen wurde in einer anderen Client Anwendung angezeigt.                                                             |
| 7     | Der Benutzer hat das Zeichen mit dem Befehl im Popup Menü des Zeichens ausgeblendet.                                 |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können diese Eigenschaft verwenden, um zu bestimmen, was bewirkt hat, dass das Zeichen verschoben wird, wenn mehr als eine Anwendung das gleiche Zeichen gemeinsam nutzt (hat geladen). Diese Werte sind identisch mit denen, die von den [**Show**](show-event.md) -und [**Hide**](hide-event.md) -Ereignissen zurückgegeben werden.

## <a name="see-also"></a>Weitere Informationen

[**Ereignis ausblenden**](hide-event.md), [**Ereignis anzeigen**](show-event.md), [**Methode ausblenden**](hide-method.md), [**Methode anzeigen**](show-method.md)


 

 




