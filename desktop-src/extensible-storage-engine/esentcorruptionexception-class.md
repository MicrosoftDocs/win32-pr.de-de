---
description: 'Weitere Informationen finden Sie unter: esentverdertionexception-Klasse'
title: EsentCorruptionException-Klasse
TOCTitle: EsentCorruptionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCorruptionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a6914c2bf133a1050e3e3800e5c113c6cac1a11f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218939"
---
# <a name="esentcorruptionexception-class"></a>EsentCorruptionException-Klasse

Basisklasse für Beschädigungen von Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentdataexception](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. esentverdertionexception  
            

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentCorruptionException _
    Inherits EsentDataException
'Usage
Dim instance As EsentCorruptionException
```

``` csharp
[SerializableAttribute]
public abstract class EsentCorruptionException : EsentDataException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentverdertionexception-Member](./esentcorruptionexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Abgeleitete Typen

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentdataexception](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. esentverdertionexception  
            [Microsoft. ISAM. ESENT. Interop. esentbademptypageexception](./esentbademptypageexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbadpagelinkexception](./esentbadpagelinkexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbadparentpagelinkexception](./esentbadparentpagelinkexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcatalogverdertedexception](./esentcatalogcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcheckpointbeschädigen TException](./esentcheckpointcorruptexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcommittedlogfilebeschädigen TException](./esentcommittedlogfilecorruptexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcommittedlogfilesmissingexception](./esentcommittedlogfilesmissingexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasebufferdependenciescorruptedexception](./esentdatabasebufferdependenciescorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasecorruptedexception](./esentdatabasecorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdbtimeverdertedexception](./esentdbtimecorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDecompressionFailedException](./esentdecompressionfailedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentderivedcolumnkorruptionexception](./esentderivedcolumncorruptionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdiskleseverificationfailureexception](./esentdiskreadverificationfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentfileiobeyonentofexception](./esentfileiobeyondeofexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentfilesystemkorruptionexception](./esentfilesystemcorruptionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindexbuildverdertedexception](./esentindexbuildcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidlogsequenceexception](./esentinvalidlogsequenceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlogkorruptduringhardrecoveryexception](./esentlogcorruptduringhardrecoveryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlogkorruptduringhardrestoreexception](./esentlogcorruptduringhardrestoreexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlogkorruptedexception](./esentlogcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlogfilebeschädigen TException](./esentlogfilecorruptexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlogreadverifyfailureexception](./esentlogreadverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlogtornschreiteduringhardrecoveryexception](./esentlogtornwriteduringhardrecoveryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlogtornschreiteduringhardrestoreexception](./esentlogtornwriteduringhardrestoreexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlvverdertedexception](./esentlvcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentmissinglogfileexception](./esentmissinglogfileexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentmissingpreviouslogfileexception](./esentmissingpreviouslogfileexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentpagenotinitializedexception](./esentpagenotinitializedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentprimaryindexverdertedexception](./esentprimaryindexcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlelostflushverifyfailureexception](./esentreadlostflushverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlupgnoverifyfailureexception](./esentreadpgnoverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentleserverifyfailureexception](./esentreadverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrecordformatsubversionfailedexception](./esentrecordformatconversionfailedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentherstellyverifyfailureexception](./esentrecoveryverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentredoabruptendedexception](./esentredoabruptendedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentsecondaryindexverdertedexception](./esentsecondaryindexcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentspavailextverdertedexception](./esentspavailextcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentspownextverdertedexception](./esentspownextcorruptedexception-class.md)