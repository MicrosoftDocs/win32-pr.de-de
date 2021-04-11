---
title: Raiserequesterrors (Eigenschaft)
description: Raiserequesterrors (Eigenschaft)
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9e559f999db663a8a9f5874f6d16a10e1e78ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104209188"
---
# <a name="raiserequesterrors-property"></a>Raiserequesterrors (Eigenschaft)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück oder legt fest, ob Fehler für Anforderungen ausgelöst werden.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent * * *. Raiserequesterrors* *  \[  =  *boolescher* Wert\]



| Teil      | BESCHREIBUNG                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Wert, der bestimmt, ob Fehler in Anforderungen ausgelöst werden.<br/> **True**    (Standard) Anforderungs Fehler werden ausgelöst. <br/> **False**     Anforderungs Fehler werden nicht ausgelöst.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mit dieser Eigenschaft können Sie feststellen, ob der Server Fehler auslöst, die mit Methoden auftreten, die [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekte unterstützen. Wenn Sie z. b. einen Animations Namen angeben, der nicht in einer [**Wiedergabe**](play-method.md)Methode vorhanden ist, löst der Server einen Fehler aus (der die Fehlermeldung anzeigt), es sei denn, Sie legen diese Eigenschaft auf **false** fest.

Dies kann für Programmiersprachen nützlich sein, die keine Wiederherstellung bereitstellen, wenn ein Fehler ausgelöst wird. Achten Sie jedoch darauf, dass Sie diese Eigenschaft auf **false** festlegen, da es möglicherweise schwieriger ist, Fehler im Code zu finden.

 

