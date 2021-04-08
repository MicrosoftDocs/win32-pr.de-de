---
description: Die getobjecttext- \_ Methode des-Objekts von "Swap-LastError" gibt ein Text Rendering des-Objekts in einem Managed Object Format-Format (MOF) zurück.
ms.assetid: efe3f3f6-c2f2-4295-bbf3-60d5b06ef98f
ms.tgt_platform: multiple
title: SWbemLastError.GetObjectText_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4247b5212e453c2f4393c26cd5ad63f07992c75a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959907"
---
# <a name="swbemlasterrorgetobjecttext_-method"></a>Methode ' Swap. getobjecttext ' \_

Die **getobjecttext \_** -Methode des-Objekts von " [**Swap-LastError**](swbemlasterror.md) " gibt ein Text Rendering des-Objekts in einem Managed Object Format-Format [(MOF)](managed-object-format--mof-.md) zurück. Dieses MOF-Objekt kann verwendet werden, um den Inhalt eines Objekts anzuzeigen. Beachten Sie, dass der MOF-Text, der zurückgegeben wird, nicht alle Informationen über das Objekt enthält, sondern nur genügend Informationen für den MOF-Compiler, um das ursprüngliche Objekt neu erstellen zu können. Sie finden beispielsweise keine Informationen zu den weiter gegebenen Qualifizierern oder den Eigenschaften der übergeordneten Klasse.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Dieser Parameter ist reserviert und muss 0 (null) sein, wenn angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung gibt diese Methode eine Zeichenfolge zurück, die den Ausgabetext enthält.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **\_ getobjecttext** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch Fehler<br/>                                                        |
| IID<br/>                      | IID \_ iswbemlasterror<br/>                                                         |



 

 




