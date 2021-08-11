---
title: RaiseRequestErrors-Eigenschaft
description: RaiseRequestErrors-Eigenschaft
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081a47eef17378c24df5bdbcb0f5141b0dece45ec9933f289d0b3da9193793d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246613"
---
# <a name="raiserequesterrors-property"></a>RaiseRequestErrors-Eigenschaft

\[Microsoft Agent ist ab Version Windows 7 veraltet und möglicherweise in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück oder legt fest, ob Fehler für Anforderungen ausgelöst werden.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent**. Boolescher RaiseRequestErrors-Wert* *  \[  =  \]



| Teil      | BESCHREIBUNG                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Wert, der bestimmt, ob Fehler in Anforderungen ausgelöst werden.<br/> **True**    (Standard) Anforderungsfehler werden ausgelöst. <br/> **False**     Anforderungsfehler werden nicht ausgelöst.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Mit dieser Eigenschaft können Sie bestimmen, ob der Server Fehler bei Methoden löst, die [**Anforderungsobjekte**](/windows/desktop/lwef/the-request-object) unterstützen. Wenn Sie beispielsweise einen Animationsnamen angeben, der in einer [**Play-Methode**](play-method.md)nicht vorhanden ist, löst der Server einen Fehler aus (die Fehlermeldung wird angezeigt), es sei denn, Sie legen diese Eigenschaft auf **False fest.**

Dies kann für Programmiersprachen nützlich sein, die keine Wiederherstellung bereitstellen, wenn ein Fehler ausgelöst wird. Verwenden Sie jedoch Vorsicht, wenn Sie diese Eigenschaft auf **False festlegen,** da es schwieriger sein kann, Fehler im Code zu finden.

 

