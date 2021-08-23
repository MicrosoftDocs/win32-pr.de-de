---
title: Vol Tag
description: Vol Tag
ms.assetid: a6444eb2-79c2-4c86-8474-846d908479df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097d03b7bb536ada8dc783e1506ba4bedfd54c6b5698e1aa68dfe55fd1f939d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035978"
---
# <a name="vol-tag"></a>Vol Tag

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Legt das Grundlegende Sprechvolumen der Sprachausgabe fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**\\ Vol=**_number_*_\\_*



| Teil     | Beschreibung                                                         |
|----------|---------------------------------------------------------------------|
| *Zahl* | Grundsprechvolumen: 0 ist Stille und 65535 ist die maximale Lautstärke. |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Die Volumeeinstellung wirkt sich sowohl auf den linken als auch auf den rechten Kanal aus. Sie können das Volume der einzelnen Kanäle nicht separat festlegen. Dieses Tag wird nur für TTS-generierte Ausgaben unterstützt.

 

 




