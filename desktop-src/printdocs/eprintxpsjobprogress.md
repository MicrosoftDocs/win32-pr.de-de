---
description: Gibt an, was der Spooler derzeit bei der Verarbeitung eines XPS-Druckauftrags tut.
ms.assetid: 4fa5b749-e4f9-4f08-97b5-e58f82d0b485
title: EPrintXPSJobProgress-Enumeration (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobProgress
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ef3d72d983388c022afbb0e914f87a17587f70b8e175dd57dabcd61d224e93bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949640"
---
# <a name="eprintxpsjobprogress-enumeration"></a>EPrintXPSJobProgress-Enumeration

Gibt an, was der Spooler derzeit bei der Verarbeitung eines XPS-Druckauftrags tut.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagEPrintXPSJobProgress { 
  kAddingDocumentSequence,
  kDocumentSequenceAdded,
  kAddingFixedDocument,
  kFixedDocumentAdded,
  kAddingFixedPage,
  kFixedPageAdded,
  kResourceAdded,
  kFontAdded,
  kImageAdded,
  kXpsDocumentCommitted
} EPrintXPSJobProgress;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**
</dt> <dd>

Eine Dokumentsequenz wird dem XPS-Auftrag hinzugefügt.

</dd> <dt>

<span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**
</dt> <dd>

Dem XPS-Auftrag wurde eine Dokumentsequenz hinzugefügt.

</dd> <dt>

<span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**
</dt> <dd>

Dem XPS-Auftrag wird ein festes Dokument hinzugefügt.

</dd> <dt>

<span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**
</dt> <dd>

Dem XPS-Auftrag wurde ein festes Dokument hinzugefügt.

</dd> <dt>

<span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**
</dt> <dd>

Dem XPS-Auftrag wird eine Seite hinzugefügt.

</dd> <dt>

<span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**
</dt> <dd>

Dem XPS-Auftrag wurde eine Seite hinzugefügt.

</dd> <dt>

<span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**
</dt> <dd>

Dem XPS-Auftrag wurde eine Ressource hinzugefügt.

</dd> <dt>

<span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**
</dt> <dd>

Dem XPS-Auftrag wurde eine Schriftart hinzugefügt.

</dd> <dt>

<span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**
</dt> <dd>

Dem XPS-Auftrag wurde ein Image hinzugefügt.

</dd> <dt>

<span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**
</dt> <dd>

Für die Daten für den XPS-Auftrag wurde ein Commit ausgeführt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration wird hauptsächlich als Parameter für die [**ReportJobProcessingProgress-Funktion**](reportjobprocessingprogress.md) verwendet.

Diese Werte können auf die Spooling- oder Renderingphase eines Druckauftrags verweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



 

 




