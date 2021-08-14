---
title: MoveCause-Eigenschaft
description: MoveCause-Eigenschaft
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa797338e64edfd67ae2347f2983df624464df923a64883e3adc5143671b15dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883831"
---
# <a name="movecause-property"></a>MoveCause-Eigenschaft

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen ganzzahligen Wert zurück, der angibt, was die letzte Bewegung des Zeichens verursacht hat.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*-Agent.* **Characters("**_CharacterID_*_"). MoveCause_*



| Wert | BESCHREIBUNG                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| 0     | Das Zeichen wurde nicht verschoben.                                                          |
| 1     | Der Benutzer hat das Zeichen verschoben.                                                              |
| 2     | Die Anwendung hat das Zeichen verschoben.                                                      |
| 3     | Das Zeichen wurde von einer anderen Clientanwendung verschoben.                                            |
| 4     | Der -Agent-Server hat das Zeichen verschoben, um es nach einer Änderung der Bildschirmauflösung auf dem Bildschirm zu halten. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können diese Eigenschaft verwenden, um zu bestimmen, was das Verschieben des Zeichens verursacht hat, wenn mehrere Anwendungen dasselbe Zeichen gemeinsam nutzen (geladen hat). Diese Werte sind mit denen identisch, die vom [**Move-Ereignis zurückgegeben**](move-event.md) werden.

## <a name="see-also"></a>Weitere Informationen

[**Move-Ereignis,**](move-event.md) [ **MoveTo-Methode**](moveto-method.md)


 

 




