---
title: Schnittstelle (com)
description: Ein optionaler Eintrag, der alle von der zugeordneten-Klasse unterstützten Schnittstellen-IDs (IIDs) angibt.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- COM-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990c06285d60067c9a26faffabffc70cbdd283d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106340754"
---
# <a name="interface-com"></a>Schnittstelle (com)

Ein optionaler Eintrag, der alle von der zugeordneten-Klasse unterstützten Schnittstellen-IDs (IIDs) angibt.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Interface
         {IID1} = name1
         {IID2} = name2
         ...
```

## <a name="remarks"></a>Bemerkungen

Wenn ein Schnittstellen Name nicht in dieser Liste vorhanden ist, kann die Schnittstelle nie von einer Instanz dieser Klasse unterstützt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnittstellenschlüssel](interface-key.md)
</dt> </dl>

 

 




