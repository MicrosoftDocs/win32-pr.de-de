---
title: Schnittstelle (COM)
description: Ein optionaler Eintrag, der alle Schnittstellen-IDs (IIDs) angibt, die von der zugeordneten Klasse unterstützt werden.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- Schnittstellenregistrierungsschlüssel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d8eaa38b97896f623c8d9f245c48f8d12634f930dc193cba14d5a9217a261e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048118"
---
# <a name="interface-com"></a>Schnittstelle (COM)

Ein optionaler Eintrag, der alle Schnittstellen-IDs (IIDs) angibt, die von der zugeordneten Klasse unterstützt werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Interface
         {IID1} = name1
         {IID2} = name2
         ...
```

## <a name="remarks"></a>Hinweise

Wenn in dieser Liste kein Schnittstellenname vorhanden ist, kann die Schnittstelle nie von einer Instanz dieser Klasse unterstützt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnittstellenschlüssel](interface-key.md)
</dt> </dl>

 

 




