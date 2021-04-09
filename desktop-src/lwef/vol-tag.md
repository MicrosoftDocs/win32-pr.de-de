---
title: Vol-Tag
description: Vol-Tag
ms.assetid: a6444eb2-79c2-4c86-8474-846d908479df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7979278b2eb89c352b9e53f6141cb585fb0ed134
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036516"
---
# <a name="vol-tag"></a>Vol-Tag

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Legt das Baseline-Lautstärke der Sprachausgabe fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**\\Vol =***Zahl***\\**



| Teil     | BESCHREIBUNG                                                         |
|----------|---------------------------------------------------------------------|
| *Zahl* | Baselineversprechungvolume: 0 ist Ruhe und 65535 ist das maximale Volume. |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Die volumeeinstellung wirkt sich auf den linken und den rechten Kanal aus. Das Volume der einzelnen Kanäle kann nicht separat festgelegt werden. Dieses Tag wird nur für die von TTS generierte Ausgabe unterstützt.

 

 




