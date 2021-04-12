---
title: Aktive Eigenschaft
description: Aktive Eigenschaft
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fe5fea7d94586c9f9d5c12b3a3b11ffbd7c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206753"
---
# <a name="active-property"></a>Aktive Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück, ob es sich bei der Anwendung um den aktiven Client des Zeichens handelt und ob es sich um das oberste Zeichen handelt.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. ***Zeichen * * * * ("*** Merkmal-ID * * *"). Aktiver* *  \[  =  *Status*\]



| Teil    | BESCHREIBUNG                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *state* | Ein ganzzahliger Ausdruck, der den Zustand der Client Anwendung angibt. 0 nicht der aktive Client.<br/> 1 der aktive Client. <br/> 2 der Eingabe-aktiv-Client. (Das oberste Zeichen.)<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn mehrere Client Anwendungen dasselbe Zeichen gemeinsam verwenden, empfängt der aktive Client des Zeichens Maus Eingaben (z. b. Microsoft Agent Control [**Click**](click-event.md) -oder [DragStart](dragstart-event.md) -Ereignisse). Wenn mehrere Zeichen angezeigt werden, empfängt der aktive Client des obersten Zeichens (auch als Input-Active Client bezeichnet) Befehls Ereignisse.

Mit der Methode " [**aktivieren**](activate-method.md)" können Sie festlegen, ob Ihre Anwendung der aktive Client des Zeichens ist, oder ob Sie die Anwendung als aktiven Client für die Anwendung festlegen möchten (wodurch das Zeichen auch am höchsten ist).

## <a name="see-also"></a>Weitere Informationen

[Methode * * aktivieren * *](activate-method.md)


 

 





