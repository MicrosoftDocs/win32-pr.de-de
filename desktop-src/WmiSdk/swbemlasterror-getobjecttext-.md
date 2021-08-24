---
description: Die GetObjectText-Methode \_ des SWbemLastError-Objekts gibt ein Textrendering des Objekts in einem mof-Format (Managed Object Format) zurück.
ms.assetid: efe3f3f6-c2f2-4295-bbf3-60d5b06ef98f
ms.tgt_platform: multiple
title: SWbemLastError.GetObjectText_-Methode (Wbemdisp.h)
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
ms.openlocfilehash: 7f935457c6fa6566d69c10b6cb5cade914e6e81c175f7451cc6eaff5268358e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679590"
---
# <a name="swbemlasterrorgetobjecttext_-method"></a>SWbemLastError.GetObjectText-Methode \_

Die **\_ GetObjectText-Methode** des [**SWbemLastError-Objekts**](swbemlasterror.md) gibt ein Textrendering des Objekts in einem [mof-Format (Managed Object Format)](managed-object-format--mof-.md) zurück. Dieses MOF-Objekt kann verwendet werden, um den Inhalt eines Objekts anzuzeigen. Beachten Sie, dass der zurückgegebene MOF-Text nicht alle Informationen zum Objekt enthält, sondern nur genügend Informationen, damit der MOF-Compiler das ursprüngliche Objekt neu erstellen kann. Beispielsweise finden Sie keine Informationen zu den weitergegebenen Qualifizierern oder den Eigenschaften der übergeordneten Klasse.

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

Dieser Parameter ist reserviert und muss bei Angabe 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Methode eine Zeichenfolge zurück, die den Ausgabetext enthält.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **\_ GetObjectText-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



 

 




