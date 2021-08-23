---
title: Page-Eigenschaft
description: Page-Eigenschaft
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ca14a4f68c326d1b231aa106450fefc7607857576f817ffaa255fa27f2249b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601009"
---
# <a name="page-property"></a>Page-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die seite zurück, die im Eigenschaftenblattfenster des Microsoft-Agents angezeigt wird, oder legt sie fest.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*agent wird. PropertySheet.Page* *  \[  =  *Zeichenfolge*\]



| Teil     | Beschreibung                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Ein Zeichenfolgenausdruck mit einem der folgenden Werte. **"Speech"** Zeigt die Seite Spracheingabe an.<br/> **"Ausgabe"** Zeigt die Seite Ausgabe an.<br/> **"Copyright"** Zeigt die Seite Copyright an.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn keine Sprach-Engine installiert ist, hat das Festlegen von **Page** auf **"Speech"** keine Auswirkungen. Außerdem muss die **Visible-Eigenschaft** des Fensters auf **True** festgelegt werden, damit der Benutzer die Seite anzeigen kann.

> [!Note]  
> Der Benutzer kann diese Eigenschaft überschreiben.

 

 

 





