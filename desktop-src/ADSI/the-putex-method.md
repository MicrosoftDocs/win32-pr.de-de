---
title: Die PutEx-Methode
description: Die IADs-PutEx-Methode verwendet den Namen einer Eigenschaft, um eine Eigenschaft mit einzelnen oder mehreren Werten im Eigenschaften Cache zu speichern.
ms.assetid: fb9a0610-e955-424b-a2b9-da4986d0ba5f
ms.tgt_platform: multiple
keywords:
- PutEx ADSI, Info
- ADSI ADSI, Beispielcode Visual Basic mit der PutEx-Methode
- Eigenschaften-ADSI, Speichern einer einzelnen Eigenschaft oder einer mehrwertigen Eigenschaft im Eigenschafts Cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea698c2dd14f3ddf8f3ad97459fad598006db22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855240"
---
# <a name="the-putex-method"></a>Die PutEx-Methode

Die [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) -Methode verwendet den Namen einer Eigenschaft, um eine Eigenschaft mit einzelnen oder mehreren Werten im Eigenschaften Cache zu speichern. Dadurch wird ein beliebiger Wert überschrieben, der sich zurzeit im Eigenschaften Cache Die Werte im Cache werden erst in den zugrunde liegenden Verzeichnisdienst geschrieben, wenn ein [**IADs:: abtinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) auftritt. Das erste Argument von **PutEx** gibt an, ob Sie vorhandene Werte für die Eigenschaft ersetzen oder hinzufügen möchten. Im folgenden Beispiel werden alle vorhandenen Werte des **Description** -Attributs im Cache gelöscht, wenn **PutEx** aufgerufen wird, und auf dem Server gelöscht, wenn " **ctinfo** " aufgerufen wird.


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



 

 




