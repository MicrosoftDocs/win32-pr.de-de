---
title: Functions (STG)
description: Funktionen sind Routinen oder Unterroutinen, die einen bestimmten Wert oder Werte zurückgeben. Strukturierte Speicherfunktionen werden in den folgenden Abschnitten beschrieben.
ms.assetid: 5fbb05ae-594d-4fa5-97d2-a2371e94c054
keywords:
- Strukturierter Speicher, Referenz, Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f49c091b5ba9619b649e620da7b436ebac4ccb
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106360459"
---
# <a name="structured-storage-functions"></a>Strukturierte Speicherfunktionen

Funktionen sind Routinen oder Unterroutinen, die einen bestimmten Wert oder Werte zurückgeben. Strukturierte Speicherfunktionen werden in den folgenden Abschnitten beschrieben:

-   [**"Kreateilockbytesonhglobal"**](/windows/desktop/api/coml2api/nf-coml2api-createilockbytesonhglobal)
-   [**"Kreatestreamonhglobal"**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
-   [**Fmtidtopropstgname**](/windows/desktop/api/coml2api/nf-coml2api-fmtidtopropstgname)
-   [**"Frepropvariantarray"**](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [**Getconvertstg**](/windows/desktop/api/coml2api/nf-coml2api-getconvertstg)
-   [**GetHGlobalFromILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-gethglobalfromilockbytes)
-   [**Gethglobalfromstream**](/windows/desktop/api/combaseapi/nf-combaseapi-gethglobalfromstream)
-   [**Oleconvertistoragetoolestream**](/windows/desktop/api/Ole2/nf-ole2-oleconvertistoragetoolestream)
-   [**Oleconvertistoragetoolestreamex**](/windows/desktop/api/Ole2/nf-ole2-oleconvertistoragetoolestreamex)
-   [**Oleconvertolestreamtoistorage**](/windows/desktop/api/Ole2/nf-ole2-oleconvertolestreamtoistorage)
-   [**Oleconvertolestreamtoistorageex**](/windows/desktop/api/Ole2/nf-ole2-oleconvertolestreamtoistorageex)
-   [**Propstgnametofmtid**](/windows/desktop/api/coml2api/nf-coml2api-propstgnametofmtid)
-   [**Propvariantclear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [**Propvariantcopy**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)
-   [**Propvariantinit**](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [**"Read classstg"**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg)
-   [**Read classstm**](/windows/desktop/api/coml2api/nf-coml2api-readclassstm)
-   [**"Read fmtusertypestg"**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg)
-   [**Stgconvertpropertyumvariant**](/windows/desktop/api/Propidl/nf-propidl-stgconvertpropertytovariant)
-   [**Setconvertstg**](/windows/desktop/api/Ole2/nf-ole2-setconvertstg)
-   [**Stgconvertvarianttoproperty**](/windows/desktop/api/Propidl/nf-propidl-stgconvertvarianttoproperty)
-   [**Stgkreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
-   [**Stgkreatedocfileonilockbytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
-   [**Stgkreatepropsetstg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
-   [**Stgkreatepropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
-   [**Stgkreatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
-   [**Stgdeserializepropvariant**](/windows/desktop/api/Propvarutil/nf-propvarutil-stgdeserializepropvariant)
-   [**Stggetifilllockbytesonfile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile)
-   [**Stggetifilllockbytesonilockbytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes)
-   [**Stgisstoragefile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile)
-   [**StgIsStorageILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgisstorageilockbytes)
-   [**Stgopenasyncdocfileonifilllockbytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes)
-   [**Stgopenlayoutdocfile**](/windows/desktop/api/Objbase/nf-objbase-stgopenlayoutdocfile)
-   [**Stgopenpropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
-   [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
-   [**Stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
-   [**StgOpenStorageOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
-   [**Stgpropertylengthasvariant**](/windows/desktop/api/Propapi/nf-propapi-stgpropertylengthasvariant)
-   [**Stgserializepropvariant**](/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant)
-   [**Stgsettimes**](/windows/desktop/api/coml2api/nf-coml2api-stgsettimes)
-   [**Schreibclassstg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg)
-   [**Schreib classstm**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstm)
-   [**"Schreibfmtusertypestg"**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg)

 

 
