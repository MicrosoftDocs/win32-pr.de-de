---
description: 'CPosPassThru.CPosPassThru-Konstruktor : Konstruktormethode.'
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: CPosPassThru.CPosPassThru-Konstruktor
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
ms.openlocfilehash: 2a6c49b305b3c6638aeaaee1480d0b561fd8c99a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085598"
---
# <a name="cpospassthrucpospassthru-constructor"></a>CPosPassThru.CPosPassThru-Konstruktor

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

Zeiger auf den Namen des Objekts zu Debugzwecken. Ordnen Sie diesen Parameter im statischen Speicher zu.

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle des aggregierenden** Objekts. Legen Sie andernfalls diesen Parameter auf **NULL fest.**

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.** Ignoriert.

</dd> <dt>

*pPin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Eingabepins des Filters.

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



