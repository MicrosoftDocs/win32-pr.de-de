---
title: CTX-Tag
description: CTX-Tag
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16beae0fd4ccc062969d9aafb4d8747e4c5afe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037202"
---
# <a name="ctx-tag"></a>CTX-Tag

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Legt den Kontext des Ausgabe Textes fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

\\**Ctx** = *Zeichenfolge*\\



| Teil     | BESCHREIBUNG                                                                                                                                                                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Eine Zeichenfolge, die den Text Kontext des nachfolgenden Texts angibt, der bestimmt, wie Symbole oder Abkürzungen gesprochen werden.<br/> **"Address"**    Adressen und/oder Telefonnummern.<br/> **"E-Mail"**    Elektronische e-Mail.<br/> Der Kontext **"unknown"** (Standard) ist unbekannt.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Dieses Tag wird nur für die von TTS generierte Ausgabe unterstützt. Der Wertebereich für den-Parameter kann abhängig von der installierten TTS-Engine variieren.

 

 





