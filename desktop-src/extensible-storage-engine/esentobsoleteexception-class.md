---
description: 'Weitere Informationen finden Sie unter: esentobsoleteexception-Klasse'
title: EsentObsoleteException-Klasse
TOCTitle: EsentObsoleteException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentObsoleteException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102357
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9d9597c3022d18ba0c6d476710f1c43430babc2
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104530437"
---
# <a name="esentobsoleteexception-class"></a>EsentObsoleteException-Klasse

Basisklasse für veraltete Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentapiexception](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. esentobsoleteexception  
            

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentObsoleteException _
    Inherits EsentApiException
'Usage
Dim instance As EsentObsoleteException
```

``` csharp
[SerializableAttribute]
public abstract class EsentObsoleteException : EsentApiException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentobsoleteexception-Member](./esentobsoleteexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Abgeleitete Typen

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentapiexception](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. esentobsoleteexception  
            [Microsoft. ISAM. ESENT. Interop. esentaccessdeniedexception](./esentaccessdeniedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbadbackupdatabasesizeexception](./esentbadbackupdatabasesizeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbadbookmarkexception](./esentbadbookmarkexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbaddbsignatureexception](./esentbaddbsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbadpatchpageexception](./esentbadpatchpageexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbadslvsignatureexception](./esentbadslvsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcannotaddfixedvarcolumninderivedtableexception](./esentcannotaddfixedvarcolumntoderivedtableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcannotnestdistributedtransaktionsexception](./esentcannotnestdistributedtransactionsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcolumnindexedexception](./esentcolumnindexedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcolumninrelationshipexception](./esentcolumninrelationshipexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcolumnlongexception](./esentcolumnlongexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcontainernotemptyexception](./esentcontainernotemptyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentchangecystackouesf memoryexception](./esentcurrencystackoutofmemoryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabase200FormatException](./esentdatabase200formatexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabase400FormatException](./esentdatabase400formatexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabase500FormatException](./esentdatabase500formatexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabaseidinuseexception](./esentdatabaseidinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasepatchfilemismatchexception](./esentdatabasepatchfilemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasesnotfromsamesnapshotexception](./esentdatabasesnotfromsamesnapshotexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasestreamingfilemismatchexception](./esentdatabasestreamingfilemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabaseunavailableexception](./esentdatabaseunavailableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatahaschangedexception](./esentdatahaschangedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdistributedtransaktionalleserypreparedumcommitexception](./esentdistributedtransactionalreadypreparedtocommitexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdistributedtransaktionnotyetprepareddecommitexception](./esentdistributedtransactionnotyetpreparedtocommitexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdtccallbackunexpectederrorexception](./esentdtccallbackunexpectederrorexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdtcmissingcallbackexception](./esentdtcmissingcallbackexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdtcmissingcallbackonherstellyexception](./esentdtcmissingcallbackonrecoveryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentfilecloseexception](./esentfilecloseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentfileioabortexception](./esentfileioabortexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentfileiofailexception](./esentfileiofailexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentfileioretryexception](./esentfileioretryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentfileiosparseexception](./esentfileiosparseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindexcantbuildexception](./esentindexcantbuildexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindextuplestoomanycolumnsexception](./esentindextuplestoomanycolumnsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidcountryexception](./esentinvalidcountryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvaliddateinameexception](./esentinvalidfilenameexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidlogdirectoriyexception](./esentinvalidlogdirectoryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidloggedoperationexception](./esentinvalidloggedoperationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidobjectexception](./esentinvalidobjectexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidonsortexception](./esentinvalidonsortexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidsystempathexception](./esentinvalidsystempathexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentkeyboundaryexception](./esentkeyboundaryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentkeyesobigexception](./esentkeytoobigexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlanguagenotsupportedexception](./esentlanguagenotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlinklotsupportedexception](./esentlinknotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlogbufferdeosmallexception](./esentlogbuffertoosmallexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentmissingpatchpageexception](./esentmissingpatchpageexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMustCommitDistributedTransactionToLevel0Exception](./esentmustcommitdistributedtransactiontolevel0exception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentmustdisableloggingfordbupgradeexception](./esentmustdisableloggingfordbupgradeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentnotindistributedtransaktionexception](./esentnotindistributedtransactionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentobjectduplicateexception](./esentobjectduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentpageboundaryexception](./esentpageboundaryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentpatchfilemissingexception](./esentpatchfilemissingexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrfsfailureexception](./esentrfsfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrfsnotarmedexception](./esentrfsnotarmedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrollbackrequirements dexception](./esentrollbackrequiredexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvbufferdeosmallexception](./esentslvbuffertoosmallexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvcolumncannotdeleteexception](./esentslvcolumncannotdeleteexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvcolumndefaultvaluenotallowedexception](./esentslvcolumndefaultvaluenotallowedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvbeschädigen tedexception](./esentslvcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvdatabasemissingexception](./esentslvdatabasemissingexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvealistkorruptexception](./esentslvealistcorruptexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvealistdeobigexception](./esentslvealisttoobigexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvealistzerozucationexception](./esentslvealistzeroallocationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvfileaccessdeniedexception](./esentslvfileaccessdeniedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvfilinput useexception](./esentslvfileinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvfileinvalidpathexception](./esentslvfileinvalidpathexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvfileioexception](./esentslvfileioexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvfile otfoundexception](./esentslvfilenotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvfilestaleexception](./esentslvfilestaleexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvfileunknownexception](./esentslvfileunknownexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvheaderbadchecksumexception](./esentslvheaderbadchecksumexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvheaderkorruptedexception](./esentslvheadercorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvinvalidpathexception](./esentslvinvalidpathexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvownermapalleseryexistsexception](./esentslvownermapalreadyexistsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvownermapverdertedexception](./esentslvownermapcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvownermappagenotfoundexception](./esentslvownermappagenotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvpgesnotcommittedexception](./esentslvpagesnotcommittedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvpgesnotdeletedexception](./esentslvpagesnotdeletedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvpgesnotfreexception](./esentslvpagesnotfreeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvpgesnotreservedexception](./esentslvpagesnotreservedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvprovidernotloadedexception](./esentslvprovidernotloadedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvproviderversionmismatchexception](./esentslvproviderversionmismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvleserverifyfailureexception](./esentslvreadverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvrootnotspecifiedexception](./esentslvrootnotspecifiedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvrootpathinvalidexception](./esentslvrootpathinvalidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvrootstillopenexception](./esentslvrootstillopenexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvspacecorruptedexception](./esentslvspacecorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvspaceschreiteconflictexception](./esentslvspacewriteconflictexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvstreamingfilealleseryexistsexception](./esentslvstreamingfilealreadyexistsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvstreamingfilefullexception](./esentslvstreamingfilefullexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvstreamingfileingeuseexception](./esentslvstreamingfileinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvstreamingfilemissingexception](./esentslvstreamingfilemissingexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvstreamingdaterdatentoedexception](./esentslvstreamingfilenotcreatedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentslvstreamingfilereadonlyexception](./esentslvstreamingfilereadonlyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentsoftrecoveryonsnapshotexception](./esentsoftrecoveryonsnapshotexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentspavailextcacheouesschmemoryexception](./esentspavailextcacheoutofmemoryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentspavailextcacheoudef SyncException](./esentspavailextcacheoutofsyncexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentsqllinklotsupportedexception](./esentsqllinknotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentstreamingdatanotloggedexception](./esentstreamingdatanotloggedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esenttaggednotnullexception](./esenttaggednotnullexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esenttempfileopenerrorexception](./esenttempfileopenerrorexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentesomanyopendatabasesexception](./esenttoomanyopendatabasesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentesomanysplitsexception](./esenttoomanysplitsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentunicodetranslationbufferdeosmallexception](./esentunicodetranslationbuffertoosmallexception-class.md)