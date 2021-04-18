---
title: Top-Eigenschaft (Zeichen-Objekt)
description: Top-Eigenschaft
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef724c7052ad1d9ba5cb51ea46ccd7647723ed32
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106338307"
---
# <a name="top-property-characters-object"></a>Top-Eigenschaft (Zeichen-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den oberen Rand des Frames des angegebenen Zeichens zurück oder legt ihn fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("**_Merkmal-ID_*_"). Top_- *  \[  =  *Wert*\]



| Teil    | BESCHREIBUNG                                             |
|---------|---------------------------------------------------------|
| *value* | Eine lange ganze Zahl, die den oberen Rand des Zeichens angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Top** -Eigenschaft wird immer in Pixel ausgedrückt, relativ zum Bildschirm Ursprung (oben links). Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens.

Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert der Speicherort des Zeichens auf den externen Dimensionen des rechteckigen Animations Rahmens, der verwendet wurde, als das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wurde.

Verwenden Sie die Methode " [**muveto**](moveto-method.md) ", um den Speicherort des Zeichens zu ändern.

## <a name="see-also"></a>Weitere Informationen

[**Left-Eigenschaft**](left-property.md), " [ **muveto** "-Methode](moveto-method.md)


 

 




