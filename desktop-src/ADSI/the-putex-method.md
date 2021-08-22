---
title: Die PutEx-Methode
description: Die PutEx-Methode der IADs verwendet den Namen einer Eigenschaft, um eine Eigenschaft mit einem oder mehreren Werten im Eigenschaftencache zu speichern.
ms.assetid: fb9a0610-e955-424b-a2b9-da4986d0ba5f
ms.tgt_platform: multiple
keywords:
- PutEx ADSI , Informationen
- ADSI ADSI, Beispielcode Visual Basic mithilfe der PutEx-Methode
- ADSI-Eigenschaften, Speichern einer einwertigen oder mehrwertigen Eigenschaft im Eigenschaftencache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646c07fad5d22110d345b71a763add5483d7f0be5f6ae2c36557eb7f1563561c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023168"
---
# <a name="the-putex-method"></a>Die PutEx-Methode

Die [**IADs::P utEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-putex) verwendet den Namen einer Eigenschaft, um eine Eigenschaft mit einem oder mehreren Werten im Eigenschaftencache zu speichern. Dadurch werden alle werte überschrieben, die sich derzeit im Eigenschaftencache befinden. Die Werte im Cache werden erst in den zugrunde liegenden Verzeichnisdienst geschrieben, wenn eine [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) auftritt. Das erste Argument von **PutEx** gibt an, ob Sie vorhandene Werte für die Eigenschaft ersetzen oder vorhandenen Werten hinzufügen möchten. Im folgenden Beispiel werden alle  vorhandenen Werte des description-Attributs im Cache gelöscht, wenn **PutEx** aufgerufen wird, und auf dem Server gelöscht, wenn **SetInfo** aufgerufen wird.


```VB
Dim x As IADs
Set x = GetObject("LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com")
'----------------------------------------------
' Assume the otherHomePhoneNumber has the following values:
' 111-1111, 222-2222
'----------------------------------------------
x.PutEx ADS_PROPERTY_APPEND, "OtherhomePhone", Array("333-3333" )  
x.SetInfo              'Now the values are 111-1111,222-222,333-3333.
 
x.PutEx ADS_PROPERTY_DELETE, "OtherHomePhone", Array("111-1111", "222-2222")
x.SetInfo              'Now the values are 333-3333.
x.PutEx ADS_PROPERTY_UPDATE, "OtherHomePhone", Array("888-8888", "999-9999")
x.SetInfo              'Now the values are 888-8888,999-9999.
x.PutEx ADS_PROPERTY_CLEAR, "OtherHomePhone",  vbNull
x.SetInfo              'Now the property has no value.
```



 

 




