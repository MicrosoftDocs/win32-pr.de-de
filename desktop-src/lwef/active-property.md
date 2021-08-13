---
title: Active-Eigenschaft
description: Active-Eigenschaft
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac75a83724c793f2a7aba01718d57e47b25a0dd6b467ca7797ad6f0e4ced018e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753169"
---
# <a name="active-property"></a>Active-Eigenschaft

\[Microsoft Agent ist ab Version Windows 7 veraltet und möglicherweise in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück, ob Ihre Anwendung der aktive Client des Zeichens ist und ob das Zeichen am weitesten oben steht.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters*("**_CharacterID_*_"). Aktiver_ *  \[  =  *Zustand*\]



| Teil    | Beschreibung                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *state* | Ein ganzzahliger Ausdruck, der den Zustand Ihrer Clientanwendung angibt. 0 Nicht der aktive Client.<br/> 1 Der aktive Client. <br/> 2 Der eingabeaktive Client. (Das oberste Zeichen.)<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn mehrere Clientanwendungen dasselbe Zeichen verwenden, empfängt der aktive Client des [](click-event.md) Zeichens Mauseingaben (z. B. Click- oder DragStart-Ereignisse des Microsoft [Agent-Steuerelements).](dragstart-event.md) Wenn mehrere Zeichen angezeigt werden, empfängt der aktive Client des obersten Zeichens (auch als eingabeaktiver Client bezeichnet) Command-Ereignisse.

Sie können die [**Activate-Methode**](activate-method.md)verwenden, um zu bestimmen, ob Ihre Anwendung der aktive Client des Zeichens ist, oder um Ihre Anwendung zum aktiven Eingabeclient zu machen (wodurch auch das Zeichen ganz oben steht).

## <a name="see-also"></a>Weitere Informationen

[Activate**-Methode**](activate-method.md)


 

 





