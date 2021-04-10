---
title: Caption-Eigenschaft (Commands-Auflistungs Objekt)
description: Caption-Eigenschaft
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010fe051568f71c4940b4bcf964f257ba9f52ca
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102687"
---
# <a name="caption-property-commands-collection-object"></a>Caption-Eigenschaft (Commands-Auflistungs Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Bestimmt den Text, der für ein [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Objekt im Popupmenü des Zeichens angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("**_Merkmal-ID_*_")._ * [Commands. Caption](caption-property.md) - \[  =  *Zeichenfolge*\]



| Teil     | BESCHREIBUNG                                                              |
|----------|--------------------------------------------------------------------------|
| *string* | Ein Zeichen folgen Ausdruck, der den Text ergibt, der als Beschriftung angezeigt wird. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie die [**Caption**](caption-property.md) -Eigenschaft für die [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung festlegen, wird definiert, wie diese im Popup Menü des Zeichens angezeigt wird, wenn die [**sichtbare**](visible-property.md) Eigenschaft auf true festgelegt ist und die Anwendung nicht der Eingabe-aktiv-Client ist. Um einen Zugriffsschlüssel (unline-mnetmonic) für Ihre **Beschriftung** anzugeben, fügen Sie vor diesem Zeichen ein kaufmännisches und-Zeichen (&) ein.

Wenn Sie Befehle für eine [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung definieren, die über eine [**Beschriftung**](caption-property.md)verfügt, definieren Sie in der Regel auch eine **Beschriftung** für die zugeordnete **Befehls** Auflistung.

 

 
