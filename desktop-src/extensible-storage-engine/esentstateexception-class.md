---
description: 'Weitere Informationen finden Sie unter: esentstateexception-Klasse'
title: EsentStateException-Klasse
TOCTitle: EsentStateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102986
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5815c3b308874f69eab9dcc7b3803ee24f6831b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218937"
---
# <a name="esentstateexception-class"></a>EsentStateException-Klasse

Basisklasse für Zustands Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentapiexception](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. esentstateexception  
            

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentStateException _
    Inherits EsentApiException
'Usage
Dim instance As EsentStateException
```

``` csharp
[SerializableAttribute]
public abstract class EsentStateException : EsentApiException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentstateexception-Member](./esentstateexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Abgeleitete Typen

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentapiexception](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. esentstateexception  
            [Microsoft. ISAM. ESENT. Interop. esentbackupinprogressexception](./esentbackupinprogressexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbackupnotallowedyetexception](./esentbackupnotallowedyetexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbaditagsequenceexception](./esentbaditagsequenceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbufferdeosmallexception](./esentbuffertoosmallexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcallbackfailedexception](./esentcallbackfailedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasealleseryupgradedexception](./esentdatabasealreadyupgradedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasefailedinkrementalreseedexception](./esentdatabasefailedincrementalreseedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasincompleteupgrade Exception](./esentdatabaseincompleteupgradeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabaseleakinspaceexception](./esentdatabaseleakinspaceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdirtyshutdownexception](./esentdirtyshutdownexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentfilename otfoundexception](./esentfilenotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindexinuseexception](./esentindexinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindexnotfoundexception](./esentindexnotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidbuffersizeexception](./esentinvalidbuffersizeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidlogdatasequenceexception](./esentinvalidlogdatasequenceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentkeyduplicateexception](./esentkeyduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentkeytrunalisiedexception](./esentkeytruncatedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogFileSizeMismatchDatabasesConsistentException](./esentlogfilesizemismatchdatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogSectorSizeMismatchDatabasesConsistentException](./esentlogsectorsizemismatchdatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlsnotsetexception](./esentlsnotsetexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentmissingfullbackupexception](./esentmissingfullbackupexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentmultivaluedduplicateaftertruncationexception](./esentmultivaluedduplicateaftertruncationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentmultivaluedduplicateexception](./esentmultivaluedduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentnoattachmentsfailedinkrementalreseedexception](./esentnoattachmentsfailedincrementalreseedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentnobackupexception](./esentnobackupexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentnocurrentrecordexception](./esentnocurrentrecordexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentobjectnotfoundexception](./esentobjectnotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentossnapshotnotallowedexception](./esentossnapshotnotallowedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrecorddeletedexception](./esentrecorddeletedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrecordnotfoundexception](./esentrecordnotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrecorddeobigexception](./esentrecordtoobigexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrecordtoobigforbackwardcompatibilityexception](./esentrecordtoobigforbackwardcompatibilityexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentherstelledwitherrorsexception](./esentrecoveredwitherrorsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRecoveredWithoutUndoDatabasesConsistentException](./esentrecoveredwithoutundodatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentherstelledwithoutundoexception](./esentrecoveredwithoutundoexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrestoreingeprogressexception](./esentrestoreinprogressexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentseparatedlongvalueexception](./esentseparatedlongvalueexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentsurrogatebackupinprogressexception](./esentsurrogatebackupinprogressexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esenttableduplicateexception](./esenttableduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esenttableinuseexception](./esenttableinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esenttestinjectionnotsupportedexception](./esenttestinjectionnotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentschreiteconflictexception](./esentwriteconflictexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentschreiteconflictprimaryindexexception](./esentwriteconflictprimaryindexexception-class.md)