---
title: Lesezeichenereignis
description: Lesezeichenereignis
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6a6dcd072b87c6a924c8d33e6ebb73c75c927bdf955f51612703d3fc18af79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976710"
---
# <a name="bookmark-event"></a>Lesezeichenereignis

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt auf, wenn ein Lesezeichen in einer Sprachtextzeichenfolge, die von Ihrer Anwendung definiert wurde, aktiviert wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Untergeordnetes**  \_ **Agent-Lesezeichen** **(ByVal** *BookmarkID**)**



| Teil         | BESCHREIBUNG                                     |
|--------------|-------------------------------------------------|
| *BookmarkID* | Eine lange ganze Zahl, die die Lesezeichennummer identifiziert. |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Um ein Lesezeichenereignis anzugeben, verwenden Sie die [**Speak-Methode**](speak-method.md) mit einem **Mrk-Tag** im angegebenen Text. Weitere Informationen zu Tags finden Sie unter Sprachausgabetags.

 

 




