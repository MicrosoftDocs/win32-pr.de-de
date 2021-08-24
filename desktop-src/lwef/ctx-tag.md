---
title: CTX-Tag
description: CTX-Tag
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7071994e741cb7dfd1147f163f0d7ef6299ec0dcb9d568ad068251d5a9436809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726099"
---
# <a name="ctx-tag"></a>CTX-Tag

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Legt den Kontext des Ausgabetexts fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

\\**CTX** = *string*\\



| Teil     | Beschreibung                                                                                                                                                                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Eine Zeichenfolge, die den Kontext des folgenden Texts angibt, der bestimmt, wie Symbole oder Abkürzungen gesprochen werden.<br/> **"Adresse"**    Adressen und/oder Telefonnummern.<br/> **"E-Mail"**    Elektronische E-Mail.<br/> **Der Kontext "Unbekannt"**    (Standard) ist unbekannt.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Dieses Tag wird nur für TTS-generierte Ausgaben unterstützt. Der Wertebereich für den Parameter kann je nach installierter TTS-Engine variieren.

 

 





