---
title: MRK-Tag
description: MRK-Tag
ms.assetid: 1bc04853-f919-4f6f-90c2-21ac836bb1e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805a66b9ce5863bda7b7b95317bcab9cf1d80f32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710511"
---
# <a name="mrk-tag"></a>MRK-Tag

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Definiert ein Lesezeichen im gesprochenen Text.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**\\MRK =***Zahl***\\**



| Teil     | BESCHREIBUNG                                        |
|----------|----------------------------------------------------|
| *Zahl* | Ein Long Integer-Wert, der das Lesezeichen identifiziert. |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Wenn der Server ein Lesezeichen verarbeitet, wird ein Lesezeichen Ereignis generiert. Sie müssen eine Zahl angeben, die größer als 0 (null) und nicht gleich 2147483647 oder 2147483646 ist.

 

 




