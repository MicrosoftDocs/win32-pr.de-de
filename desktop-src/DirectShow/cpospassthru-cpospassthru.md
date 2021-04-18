---
description: Konstruktormethode.
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: Cpospassthru. cpospassthru-Konstruktor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CPosPassThru
api_type:
- COM
api_location: ''
ms.openlocfilehash: ba49bd1e2f65cf0d2a8a398ecab167e74dc35ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343545"
---
# <a name="cpospassthrucpospassthru-constructor"></a>Cpospassthru. cpospassthru-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeiger auf den Namen des Objekts, zu Debuggingzwecken. Weisen Sie diesen Parameter im statischen Arbeitsspeicher zu.

</dd> <dt>

*Kro* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts. Andernfalls legen Sie diesen Parameter auf **null** fest.

</dd> <dt>

*PHR* 
</dt> <dd>

Zeiger auf einen **HRESULT** -Wert. Ignoriert.

</dd> <dt>

*ppin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Eingabe-PIN des Filters.

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



