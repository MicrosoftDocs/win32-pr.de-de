---
description: 'Weitere Informationen finden Sie unter: esentusageexception-Klasse'
title: EsentUsageException-Klasse
TOCTitle: EsentUsageException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentUsageException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103173
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentUsageException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0319ae3d6185e3075931fb601ec789aba70dfd82
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103869363"
---
# <a name="esentusageexception-class"></a>EsentUsageException-Klasse

Basisklasse für Verwendungs Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentapiexception](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. esentusageexception  
            

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentUsageException _
    Inherits EsentApiException
'Usage
Dim instance As EsentUsageException
```

``` csharp
[SerializableAttribute]
public abstract class EsentUsageException : EsentApiException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentusageexception-Member](./esentusageexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Abgeleitete Typen

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentapiexception](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. esentusageexception  
            [Microsoft. ISAM. ESENT. Interop. esentafterinitializationexception](./esentafterinitializationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentalleseryinitializedexception](./esentalreadyinitializedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentalleserypreparedexception](./esentalreadypreparedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbackupdirectoriynotemptyexception](./esentbackupdirectorynotemptyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbadcolumnidexception](./esentbadcolumnidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentbadrestoretargetinstanceexception](./esentbadrestoretargetinstanceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcallbacknotresolvedexception](./esentcallbacknotresolvedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcannotbetaggedexception](./esentcannotbetaggedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcannotdelta etesystemtableexception](./esentcannotdeletesystemtableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcannotdeletetemplatetableexception](./esentcannotdeletetemplatetableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcannotdeletetemptableexception](./esentcannotdeletetemptableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcannotdisableversioningexception](./esentcannotdisableversioningexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcannotindexexception](./esentcannotindexexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcannotmaterializeforwardonlysortexception](./esentcannotmaterializeforwardonlysortexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcannotnestddlexception](./esentcannotnestddlexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcannotseparateintrinsiclvexception](./esentcannotseparateintrinsiclvexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcolumncannotbecompressedexception](./esentcolumncannotbecompressedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcolumndoesnotfitexception](./esentcolumndoesnotfitexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcolumnduplicateexception](./esentcolumnduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcolumninuseexception](./esentcolumninuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcolumnnochunkexception](./esentcolumnnochunkexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcolumnnotfoundexception](./esentcolumnnotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcolumnnotupdatableexception](./esentcolumnnotupdatableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcolumnredundant TException](./esentcolumnredundantexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentcolumndeobigexception](./esentcolumntoobigexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasealleseryrunningmaintenanceexception](./esentdatabasealreadyrunningmaintenanceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasecorruptednorepirexception](./esentdatabasecorruptednorepairexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabaseduplicateexception](./esentdatabaseduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasefilereadonlyexception](./esentdatabasefilereadonlyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabaseingeuseexception](./esentdatabaseinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabaseingevalidinkrementalreseedexception](./esentdatabaseinvalidincrementalreseedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabaseinvalidnameexception](./esentdatabaseinvalidnameexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabaseinvalidpgesexception](./esentdatabaseinvalidpagesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabaseinvalidpathexception](./esentdatabaseinvalidpathexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabaselockedexception](./esentdatabaselockedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasenotfoundexception](./esentdatabasenotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasesharingviolationexception](./esentdatabasesharingviolationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdatabasesigninuseexception](./esentdatabasesigninuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentddlnotvererableexception](./esentddlnotinheritableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdefaultvaluetoobigexception](./esentdefaultvaluetoobigexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdensityinvalidexception](./esentdensityinvalidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdisabledfunctionalityexception](./esentdisabledfunctionalityexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esententrypointnotfoundexception](./esententrypointnotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentexclusivetablelockrequirements dexception](./esentexclusivetablelockrequiredexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentfeaturenotavailableexception](./esentfeaturenotavailableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentfilecompressedexception](./esentfilecompressedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentfilteredmuvenotsupportedexception](./esentfilteredmovenotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentfixedddlexception](./esentfixedddlexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentfixedinheritedddlexception](./esentfixedinheritedddlexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentforcedetachnotallowedexception](./esentforcedetachnotallowedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentillegaloperationexception](./esentillegaloperationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindexduplicateexception](./esentindexduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindexhasprimaryexception](./esentindexhasprimaryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindexinvaliddefexception](./esentindexinvaliddefexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindexmuststayexception](./esentindexmuststayexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindextuplescannotretrievefromindexexception](./esentindextuplescannotretrievefromindexexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindextuplesinvalidlimitsexception](./esentindextuplesinvalidlimitsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindextupleskeydeosmallexception](./esentindextupleskeytoosmallexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindextuplesnonuniqueonlyexception](./esentindextuplesnonuniqueonlyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindextuplessecondaryindexonlyexception](./esentindextuplessecondaryindexonlyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindextuplestextbinarycolumnsonlyexception](./esentindextuplestextbinarycolumnsonlyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentindextuplesvarsegmacnotallowedexception](./esentindextuplesvarsegmacnotallowedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinstancenameingeuseexception](./esentinstancenameinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentintransaktionexception](./esentintransactionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidbackupexception](./esentinvalidbackupexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidbackupsequenceexception](./esentinvalidbackupsequenceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidbookmarkexception](./esentinvalidbookmarkexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidcodepageexception](./esentinvalidcodepageexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidcolumntypeexception](./esentinvalidcolumntypeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidkreateindexexception](./esentinvalidcreateindexexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvaliddatabaseexception](./esentinvaliddatabaseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvaliddatabaseidexception](./esentinvaliddatabaseidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidgrbitexception](./esentinvalidgrbitexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidindexidexception](./esentinvalidindexidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidinstanceexception](./esentinvalidinstanceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidlanguageidexception](./esentinvalidlanguageidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidlcmapstringflagsexception](./esentinvalidlcmapstringflagsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidnameexception](./esentinvalidnameexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidoperationexception](./esentinvalidoperationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidparameterexception](./esentinvalidparameterexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidpathexception](./esentinvalidpathexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidplaceholdercolumnexception](./esentinvalidplaceholdercolumnexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidprereadexception](./esentinvalidprereadexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidsesidexception](./esentinvalidsesidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidsettingsexception](./esentinvalidsettingsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinvalidtableidexception](./esentinvalidtableidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentkeyismadecoexception](./esentkeyismadeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentkeynotmadebug Exception](./esentkeynotmadeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlogfile otcopiedexception](./esentlogfilenotcopiedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlogfilepythinuseexception](./esentlogfilepathinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlogfilesizemismatchexception](./esentlogfilesizemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentloggingdisabledexception](./esentloggingdisabledexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlsalleserysetexception](./esentlsalreadysetexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlscallbacknotspecifiedexception](./esentlscallbacknotspecifiedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentmultivaluedcolumnmustbetaggedexception](./esentmultivaluedcolumnmustbetaggedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentmultivaluedindexviolationexception](./esentmultivaluedindexviolationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentmustbeseparatelongvalueexception](./esentmustbeseparatelongvalueexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMustRollbackException](./esentmustrollbackexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentnobackupdirectoriyexception](./esentnobackupdirectoryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentnocurrentindexexception](./esentnocurrentindexexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentnotinitializedexception](./esentnotinitializedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentnotintransaktionexception](./esentnotintransactionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentnullinvalidexception](./esentnullinvalidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentnullkeydiszuzuwedexception](./esentnullkeydisallowedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentonedatabasepersessionexception](./esentonedatabasepersessionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentossnapshotinvalidsequenceexception](./esentossnapshotinvalidsequenceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentossnapshotinvalidsnapidexception](./esentossnapshotinvalidsnapidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentpartiallyattacheddbexception](./esentpartiallyattacheddbexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentpermissiondeniedexception](./esentpermissiondeniedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentquerynotsupportedexception](./esentquerynotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrecordnocopyexception](./esentrecordnocopyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrecordprimarychangedexception](./esentrecordprimarychangedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrestoreof nonbackupdatabaseexception](./esentrestoreofnonbackupdatabaseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrunninginmultiinstancemodeexception](./esentrunninginmultiinstancemodeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrunninginoneinstancemodeexception](./esentrunninginoneinstancemodeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentsesidtableidmismatchexception](./esentsesidtableidmismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentsessioncontextalleserysetexception](./esentsessioncontextalreadysetexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentsessioncontextnotsetbythisthreadexception](./esentsessioncontextnotsetbythisthreadexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentsessioninuseexception](./esentsessioninuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentsessionsharingviolationexception](./esentsessionsharingviolationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentsessionschreiteconflictexception](./esentsessionwriteconflictexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentsoftrecoveryonbackupdatabaseexception](./esentsoftrecoveryonbackupdatabaseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentspacehintsinvalidexception](./esentspacehintsinvalidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentsystemparamsalleserysetexception](./esentsystemparamsalreadysetexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentsystempythinuseexception](./esentsystempathinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esenttablelockedexception](./esenttablelockedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esenttablenotemptyexception](./esenttablenotemptyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esenttemppathinuseexception](./esenttemppathinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentesomanyactiveusersexception](./esenttoomanyactiveusersexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentesomanyattacheddatabasesexception](./esenttoomanyattacheddatabasesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentesomanycolumnsexception](./esenttoomanycolumnsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentesomanyindexesexception](./esenttoomanyindexesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentesomanykeysexception](./esenttoomanykeysexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentesomanyopentablesandcleanuptimedoutexception](./esenttoomanyopentablesandcleanuptimedoutexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentesomanytestinjectionsexception](./esenttoomanytestinjectionsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esenttransread onlyexception](./esenttransreadonlyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esenttranstoodeepexception](./esenttranstoodeepexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentunicodenormalizationnotsupportedexception](./esentunicodenormalizationnotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentupdatemustversionexception](./esentupdatemustversionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentupdatenotpreparedexception](./esentupdatenotpreparedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentversionstoreoudefimemoryandcleanuptimedoutexception](./esentversionstoreoutofmemoryandcleanuptimedoutexception-class.md)