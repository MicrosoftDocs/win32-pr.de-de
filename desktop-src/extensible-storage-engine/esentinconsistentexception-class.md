---
description: 'Weitere Informationen finden Sie unter: EsentInconsistentException-Klasse'
title: EsentInconsistentException-Klasse
TOCTitle: EsentInconsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInconsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55101798
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e62b963e5b0d3f400a860f7742bb76a183b67bd7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106351833"
---
# <a name="esentinconsistentexception-class"></a>EsentInconsistentException-Klasse

Basisklasse für inkonsistente Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentdataexception](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentInconsistentException  
            

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentInconsistentException _
    Inherits EsentDataException
'Usage
Dim instance As EsentInconsistentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentInconsistentException : EsentDataException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[EsentInconsistentException-Member](./esentinconsistentexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Abgeleitete Typen

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentdataexception](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentInconsistentException  
            [Microsoft. ISAM. ESENT. Interop. esentattacheddatabasemismatchexception](./esentattacheddatabasemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbadcheckpointsignatureexception](./esentbadcheckpointsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbadlogsignatureexception](./esentbadlogsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbadlogversionexception](./esentbadlogversionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcheckpointfile topics-Quelle](./esentcheckpointfilenotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentkonsistenttimemismatchexception](./esentconsistenttimemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasedirtyshutdownexception](./esentdatabasedirtyshutdownexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasincompleteinkrementalreseedexception](./esentdatabaseincompleteincrementalreseedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabaselogsetmismatchexception](./esentdatabaselogsetmismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdbtimedeonewexception](./esentdbtimetoonewexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdbtimedeooldexception](./esentdbtimetoooldexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentendingrestorelogopolowexception](./esentendingrestorelogtoolowexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentexistinglogfilehasbadsignatureexception](./esentexistinglogfilehasbadsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentexistinglogfileisnotcontiguousexception](./esentexistinglogfileisnotcontiguousexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentfileinvalidtypeexception](./esentfileinvalidtypeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentgivenlogfilehasbadsignatureexception](./esentgivenlogfilehasbadsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentgivenlogfileisnotcontiguousexception](./esentgivenlogfileisnotcontiguousexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidkreatedbversionexception](./esentinvalidcreatedbversionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvaliddatabaseversionexception](./esentinvaliddatabaseversionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentloggenerationmismatchexception](./esentloggenerationmismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentmissingcurrentlogfilesexception](./esentmissingcurrentlogfilesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentmissingfilebackbackupexception](./esentmissingfiletobackupexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentmissingrestorelogfilesexception](./esentmissingrestorelogfilesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentpagesizemismatchexception](./esentpagesizemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrequirements dlogfilesmissingexception](./esentrequiredlogfilesmissingexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentstartingrestorelogesohighexception](./esentstartingrestorelogtoohighexception-class.md)