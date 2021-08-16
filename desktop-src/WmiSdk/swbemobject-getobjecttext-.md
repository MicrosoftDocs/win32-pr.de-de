---
description: Die \_ GetObjectText-Methode des SWbemObject-Objekts gibt ein Textrendering des Objekts zurück.
ms.assetid: 8b980863-14ad-4884-8897-dd076d927824
ms.tgt_platform: multiple
title: SWbemObject.GetObjectText_ -Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d33e4f3f530bf7d9bda2e228243026de7d3768efb668cf6c8683690e8127f65f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992060"
---
# <a name="swbemobjectgetobjecttext_-method"></a>SWbemObject.GetObjectText-Methode \_

Die **GetObjectText-Methode \_** des [**SWbemObject-Objekts**](swbemobject.md) gibt ein Textrendering des Objekts zurück. Dieses Objekt kann verwendet werden, um den Inhalt eines Objekts anzuzeigen. Derzeit wird nur die MOF-Syntax als Ausgabeformat unterstützt. Beachten Sie, dass der zurückgegebene MOF-Text nicht alle Informationen zum Objekt enthält. Der MOF-Text enthält nur genügend Informationen, damit der MOF-Compiler das ursprüngliche Objekt neu erstellen kann. Beispielsweise gibt es keine Informationen zu den propagierten Qualifizierern oder den Eigenschaften der übergeordneten Klasse.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Reserviert und muss 0 (null) sein, wenn angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Methode eine Zeichenfolge zurück, die den Ausgabetext enthält.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **GetObjectText-Methode \_** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Ungültiger Parameter wurde angegeben.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher zum Abschließen des Vorgangs.

</dd> </dl>

## <a name="examples"></a>Beispiele

Der folgende Code, der aus dem Codebeispiel List the Definition of a WMI Class in MOF Format VBScript (Auflisten der Definition einer WMI-Klasse im [MOF-Format)](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) im TechNet-Katalog entnommen wurde, ruft die Textdarstellung einer WMI-Klassendefinition in der MOF-Syntax (Managed Object Format) ab und zeigt sie an.


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Const wbemFlagUseAmendedQualifiers = &h20000 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace) 
 
Set objClass = objWMIService.Get(strClass, wbemFlagUseAmendedQualifiers) 
strMOF = objClass.GetObjectText_ 
  
WScript.Echo strMOF 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




