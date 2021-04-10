---
title: Count-Eigenschaft
description: Count-Eigenschaft
ms.assetid: a0375aa9-495d-47be-a3f7-4d5987688555
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 630817a8370a071851216ab03d43493e672b3e0a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858191"
---
# <a name="count-property"></a>Count-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt eine lange Ganzzahl (schreibgeschützte Eigenschaft) zurück, die die Anzahl der [**Befehls**](/windows/desktop/lwef/the-command-object) Objekte in der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angibt.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). Befehle. Count**

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**Count** schließt nur die Anzahl der [**Befehls**](/windows/desktop/lwef/the-command-object) Objekte ein, die Sie in der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung definieren. Server-oder andere Client Einträge sind nicht eingeschlossen.

 

 