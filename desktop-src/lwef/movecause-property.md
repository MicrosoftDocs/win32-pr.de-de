---
title: Eigenschaft "muvecause"
description: Eigenschaft "muvecause"
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7f91d068befa2b919c04818c46dbc1a48faa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856211"
---
# <a name="movecause-property"></a>Eigenschaft "muvecause"

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen ganzzahligen Wert zurück, der angibt, was das letzte Verschieben des Zeichens verursacht hat.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent*. **Zeichen ("***Merkmal-ID***"). "Muvecause** "



| Wert | BESCHREIBUNG                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| 0     | Das Zeichen wurde nicht verschoben.                                                          |
| 1     | Der Benutzer hat das Zeichen verschoben.                                                              |
| 2     | Die Anwendung hat das Zeichen verschoben.                                                      |
| 3     | Das Zeichen wurde von einer anderen Client Anwendung verschoben.                                            |
| 4     | Der Agent-Server hat das Zeichen verschoben, um es nach einer Änderung der Bildschirmauflösung auf dem Bildschirm aufzubewahren. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können diese Eigenschaft verwenden, um zu bestimmen, was das Zeichen bewegt hat, wenn mehr als eine Anwendung das gleiche Zeichen gemeinsam nutzt (hat geladen). Diese Werte sind identisch mit denen, die vom [**Move**](move-event.md) -Ereignis zurückgegeben werden.

## <a name="see-also"></a>Weitere Informationen

[**Move-Ereignis**](move-event.md), [ **MoveTo-Methode**](moveto-method.md)


 

 




