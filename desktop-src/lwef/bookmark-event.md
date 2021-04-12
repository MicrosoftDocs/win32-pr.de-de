---
title: Bookmark-Ereignis
description: Bookmark-Ereignis
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0695ccd04f93eae46eaae66955c84fefb9e0c963
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206597"
---
# <a name="bookmark-event"></a>Bookmark-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt auf, wenn ein Lesezeichen in einer sprach Text Zeichenfolge aktiviert wird, die von der Anwendung definiert wurde

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub-** *Agent*- \_ **Lesezeichen** **(ByVal** - *BookmarkID * * *)**



| Teil         | BESCHREIBUNG                                     |
|--------------|-------------------------------------------------|
| *BookmarkID* | Eine lange ganze Zahl, die die Lesezeichen Nummer identifiziert. |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Um ein Lesezeichen Ereignis anzugeben, verwenden Sie die [**Sprech**](speak-method.md) Methode mit einem **MRK** -Tag im angegebenen Text. Weitere Informationen zu Tags finden Sie unter Sprachausgabe Tags.

 

 




