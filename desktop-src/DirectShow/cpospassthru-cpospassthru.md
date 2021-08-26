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
ms.openlocfilehash: ec75218f43edcf6c3c2c6298eba7c886cdd04879485bf41f20951cba1f9c4935
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108320"
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

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle** des aggregierenden Objekts. Legen Sie andernfalls diesen Parameter auf **NULL** fest.

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

 

 



