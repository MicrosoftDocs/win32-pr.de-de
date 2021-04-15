---
description: Gibt an, wie der Spooler gerade ausgeführt wird, während er einen XPS-Druckauftrag verarbeitet.
ms.assetid: 4fa5b749-e4f9-4f08-97b5-e58f82d0b485
title: Eprintxpsjobprogress-Enumeration (winspool. h)
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
ms.openlocfilehash: 2a09b55ed72a6276a1a9d224cc08e03546f887d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529543"
---
# <a name="eprintxpsjobprogress-enumeration"></a>Eprintxpsjobprogress-Enumeration

Gibt an, wie der Spooler gerade ausgeführt wird, während er einen XPS-Druckauftrag verarbeitet.

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

<span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kaddingdocumentsequence**
</dt> <dd>

Eine Dokument Sequenz wird dem XPS-Auftrag hinzugefügt.

</dd> <dt>

<span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kdocumentsequenceadded**
</dt> <dd>

Eine Dokument Sequenz wurde dem XPS-Auftrag hinzugefügt.

</dd> <dt>

<span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kaddingfixeddocument**
</dt> <dd>

Ein festes Dokument wird dem XPS-Auftrag hinzugefügt.

</dd> <dt>

<span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kfixeddocumentadded**
</dt> <dd>

Dem XPS-Auftrag wurde ein festes Dokument hinzugefügt.

</dd> <dt>

<span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kaddingfixedpage**
</dt> <dd>

Eine Seite wird dem XPS-Auftrag hinzugefügt.

</dd> <dt>

<span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kfixedpageadded**
</dt> <dd>

Dem XPS-Auftrag wurde eine Seite hinzugefügt.

</dd> <dt>

<span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kresourceadded**
</dt> <dd>

Dem XPS-Auftrag wurde eine Ressource hinzugefügt.

</dd> <dt>

<span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kfontadded**
</dt> <dd>

Dem XPS-Auftrag wurde eine Schriftart hinzugefügt.

</dd> <dt>

<span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kimageadded**
</dt> <dd>

Dem XPS-Auftrag wurde ein Bild hinzugefügt.

</dd> <dt>

<span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kxpsdocumentcommit**
</dt> <dd>

Für die Daten für den XPS-Auftrag wurde ein Commit ausgeführt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird primär als Parameter für die [**reportjobprocessingprogress**](reportjobprocessingprogress.md) -Funktion verwendet.

Diese Werte können entweder auf die spoolingphase oder die Renderingphase eines Druckauftrags verweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |



 

 




