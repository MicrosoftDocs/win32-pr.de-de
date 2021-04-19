---
title: Caption-Eigenschaft (Befehls Objekt)
description: Caption-Eigenschaft
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0595444bd2e49ca0207c5a6a9fd459e919573958
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341342"
---
# <a name="caption-property-command-object"></a>Caption-Eigenschaft (Befehls Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Bestimmt den Text, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object) im Popup Menü des angegebenen Zeichens angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("**_Merkmal-ID_*_"). Befehle ("_*_Name_*_"). Caption_- *  \[  =  *Zeichenfolge*\]



| Teil     | BESCHREIBUNG                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| *string* | Ein Zeichen folgen Ausdruck, der den Text ergibt, der als Beschriftung für den **Befehl** angezeigt wird. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um einen Zugriffsschlüssel (unline-mnetmonic) für Ihre **Beschriftung** anzugeben, fügen Sie vor diesem Zeichen ein kaufmännisches und-Zeichen (&) ein.

Wenn Sie keine **voicecaption** für Ihren Befehl definieren, wird die **Beschriftungs** Einstellung verwendet.

 

 
