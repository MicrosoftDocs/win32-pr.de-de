---
description: Ein Visual Basic Scripting Edition (VBScript)-Beispiel, in dem das Objekttag verwendet wird, um eine Instanz des Zertifikatregistrierungs-Steuerungs Objekts zu erstellen.
ms.assetid: 6e2a230e-81c1-4b63-9ad5-3edfc239ad7c
title: Die Zertifikat Registrierungs Steuerung wird in VBScript instanziiert.
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da14c55a3c9005f820be8f8d60026bc31ac4920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958995"
---
# <a name="the-certificate-enrollment-control-instantiated-in-vbscript"></a><span data-ttu-id="5afa3-103">Die Zertifikat Registrierungs Steuerung wird in VBScript instanziiert.</span><span class="sxs-lookup"><span data-stu-id="5afa3-103">The Certificate Enrollment Control Instantiated in VBScript</span></span>

<span data-ttu-id="5afa3-104">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird das Objekttag verwendet, um eine Instanz des Zertifikatregistrierungs-Steuerungs Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5afa3-104">The following Visual Basic Scripting Edition (VBScript) example uses the OBJECT tag to create an instance of the Certificate Enrollment Control object.</span></span> <span data-ttu-id="5afa3-105">Das Objekt wird aus dem Arbeitsspeicher freigegeben, wenn es den Gültigkeitsbereich verlässt.</span><span class="sxs-lookup"><span data-stu-id="5afa3-105">The object is freed from memory when it goes out of scope.</span></span>


```VB
<HTML>
<HEAD>
<TITLE>VBScript Certificate Enrollment Control Sample
</TITLE>
<OBJECT classid="clsid:127698E4-E730-4E5C-A2b1-21490A70C8A1"
    codebase="xenroll.dll"
    id=Enroll >
</OBJECT>
<BR>
Certificate Enrollment Control Instantiation Sample
<BR>
<BR>

<SCRIPT language="VBScript">
<!--
' Declare a local variable.
Dim varName
' Enable error handling.
On Error Resume Next
' Attempt to use the control, in this case to retrieve a property.
varName = Enroll.MyStoreName
' If above line failed, Err.Number will not be 0.
if ( Err.Number <> 0 ) then
    MsgBox("Error!")
    Err.clear
else
    ' The control property was successfully retrieved,
    ' display the property value.
    varName = "MyStoreName is " & varName
    MsgBox( varName )
end if
-->
</SCRIPT>
<BR>
</HEAD>
</HTML>
```



 

 



