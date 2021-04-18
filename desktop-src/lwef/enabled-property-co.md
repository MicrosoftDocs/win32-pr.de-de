---
title: Aktivierte Eigenschaft (Befehls Objekt)
description: Enabled-Eigenschaft
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5999e396f61fbcc820bc1cec7deb0c603eb948e4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341345"
---
# <a name="enabled-property-command-object"></a>Aktivierte Eigenschaft (Befehls Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück oder legt fest, ob der **Befehl** im Popup Menü des angegebenen Zeichens aktiviert ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("**_Merkmal-ID_*_"). Befehle ("_*_Name_*_"). Aktivierter_ *  \[  =  *boolescher* Wert\]



| Teil      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der angibt, ob der **Befehl** aktiviert ist.<br/> <dl> <dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Fall**</dt> <dd> Der **Befehl** ist aktiviert.<br/> </dd> <dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt> <dd> Der **Befehl** ist deaktiviert.<br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn die [**aktivierte**](enabled-property.md) Eigenschaft auf **true** festgelegt ist, wird die Beschriftung der [**Befehls**](/windows/desktop/lwef/the-command-object) Objekte im Popupmenü des Zeichens als normaler Text angezeigt, wenn die Client Anwendung aktiv ist. Wenn die **aktivierte** Eigenschaft **false** ist, wird die Beschriftung als nicht verfügbarer (deaktivierter) Text angezeigt. Ein deaktivierter **Befehl** ist auch für die Spracheingabe nicht zugänglich.

 

