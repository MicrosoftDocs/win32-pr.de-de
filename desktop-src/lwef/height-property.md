---
title: Height-Eigenschaft (Character-Objekt)
description: Height-Eigenschaft
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e504dcbbfd470c62b4102d86f25a1d2b3c4c25e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739321"
---
# <a name="height-property-characters-object"></a>Height-Eigenschaft (Character-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die Höhe des angegebenen Zeichen Rahmens zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("**_Merkmal-ID_*_"). Height_- *  \[ =  *Wert*\]



| Teil    | BESCHREIBUNG                                                 |
|---------|-------------------------------------------------------------|
| *value* | Eine lange ganze Zahl, die die Rahmenhöhe des Zeichens angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **height** -Eigenschaft wird immer in Pixel ausgedrückt, relativ zu Bildschirm Koordinaten (oben links). Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens.

Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert die Höhe des Zeichens auf den externen Dimensionen des rechteckigen Animations Rahmens, der verwendet wurde, als das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wurde.

 

 




