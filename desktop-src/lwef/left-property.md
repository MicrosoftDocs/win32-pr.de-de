---
title: Left-Eigenschaft (Character-Objekt)
description: Left-Eigenschaft
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a318e659405883c56f296a9371eba7e9423662b1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337897"
---
# <a name="left-property-characters-object"></a>Left-Eigenschaft (Character-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den linken Rand des Frames des angegebenen Zeichens zurück oder legt ihn fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("**_Merkmal-ID_*_"). Linker_ *  \[  =  *Wert*\]



| Teil    | BESCHREIBUNG                                                           |
|---------|-----------------------------------------------------------------------|
| *value* | Eine lange ganze Zahl, die den linken Rand des Frames des Zeichens angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **left** -Eigenschaft wird immer in Pixel ausgedrückt, relativ zum Bildschirm Ursprung (oben links). Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens.

Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert der Speicherort des Zeichens auf den externen Dimensionen des rechteckigen Animations Rahmens, der verwendet wurde, als das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wurde.

 

 




