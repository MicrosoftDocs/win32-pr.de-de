---
title: D1105 Threading Verletzung
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: Auf eine Verleih Thread Schnittstelle wurde gleichzeitig von mehreren Threads aus zugegriffen.
keywords:
- D1105 Threading Verletzung Direct2D
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe83baa32be8ae18948ae5a80e3e0b218cd4fa4a
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2021
ms.locfileid: "106370892"
---
# <a name="d1105-threading-violation"></a>D1105: Threading Verletzung

Auf eine Verleih Thread Schnittstellen \[ *Schnittstelle* \] wurde gleichzeitig von mehreren Threads aus zugegriffen.

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*berfläche*
</dt> <dd>

Die Adresse der Schnittstelle, auf die von mehreren Threads zugegriffen wurde.

</dd> </dl> 




 

## <a name="possible-causes"></a>Mögliche Ursachen

Verwenden einer Objektinstanz aus derselben Single Thread Factory aus zwei verschiedenen Threads.

 

 




