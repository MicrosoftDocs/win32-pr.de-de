---
title: D1105-Threadingverletzung
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: Auf eine RentalThreadschnittstelle wurde gleichzeitig von mehreren Threads aus zugegriffen.
keywords:
- D1105– Threadingverletzung Direct2D
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 12e7321fd40437bc262439c6ddb319a0aa6dba145d05d3feebba2813c904bbce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537970"
---
# <a name="d1105-threading-violation"></a>D1105: Threadingverletzung

Auf eine Schnittstelle mit Verleihthreadingschnittstelle \[  \] wurde gleichzeitig von mehreren Threads aus zugegriffen.

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Schnittstelle*
</dt> <dd>

Die Adresse der Schnittstelle, auf die von mehreren Threads zugegriffen wurde.

</dd> </dl> 




 

## <a name="possible-causes"></a>Mögliche Ursachen

Verwenden einer Objektinstanz aus derselben Singlethreadfactory aus zwei verschiedenen Threads.

 

 




