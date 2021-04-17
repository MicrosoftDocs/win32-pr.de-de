---
title: Pitch-Eigenschaft
description: Pitch-Eigenschaft
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 998ee4bcf77878062425086d67066040f5d58421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388762"
---
# <a name="pitch-property"></a>Pitch-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Beschreibung** 
</dt> <dd>

Gibt eine lange ganze Zahl für die Einstellung für die Sprachausgabe (TTS) der angegebenen Zeichenfolge zurück.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). Spur**

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gilt nur für Zeichen, die für die TTS-Ausgabe konfiguriert sind. Wenn das Zeichen keine TTS-Ausgabe unterstützt, gibt diese Eigenschaft 0 (null) zurück.

Obwohl Ihre Anwendung diesen Wert nicht schreiben kann, können Sie **Pit** -Tags (Pitch-Tags) in den Ausgabetext einschließen, um die Größe für eine bestimmte Äußerung vorübergehend zu erhöhen. Wenn Sie das **boxtag** zum Ändern der Tonhöhe verwenden, ändert sich die Einstellung der Eigenschaft " **Pitch** " jedoch nicht. Weitere Informationen finden Sie unter [Sprachausgabe Tags](pit-tag.md).

 

 




