---
description: Die \_ CompareTo-Methode des SWbemLastError-Objekts vergleicht zwei SWbemObject-Objekte. Dieser Vergleich unterliegt bestimmten Einschränkungen, die auf den im iFlags-Parameter angegebenen Werten basieren.
ms.assetid: 541510e4-ef8d-4436-966f-19c5df422281
ms.tgt_platform: multiple
title: SWbemLastError.CompareTo_ -Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cc169b8a18f97cd6fd8f51a0e8d1456e3619cfbebf0cbf1f107adfac2787bb54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314594"
---
# <a name="swbemlasterrorcompareto_-method"></a>SWbemLastError.CompareTo-Methode \_

Die **CompareTo-Methode \_** des [**SWbemLastError-Objekts**](swbemlasterror.md) vergleicht zwei [**SWbemObject-Objekte.**](swbemobject.md) Dieser Vergleich unterliegt bestimmten Einschränkungen, die auf den im *iFlags-Parameter angegebenen Werten* basieren.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objwbemObject* \[ In\]
</dt> <dd>

Erforderlich. Ein [**SWbemObject-Klassenobjekt.**](swbemobject.md) Dieser Parameter ist das Objekt, mit dem das erste Objekt verglichen wird. Das Objekt muss eine gültige **SWbemObject-Instanz** sein.

</dd> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Eine ganze Zahl, die zusätzliche Flags für den Vorgang angibt. Dieser Parameter gibt die Objektmerkmale an, die bei Objektvergleichen zu berücksichtigen sind. Sie können **wbemComparisonFlagIncludeAll** verwenden, um alle Features (Standard) oder eine beliebige Kombination der folgenden Werte zu berücksichtigen.

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll** (0 (0x0))


</dt> <dd>

Bewirkt, dass alle Eigenschaften, Qualifizierer und Varianten verglichen werden.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers** (1 (0x1))


</dt> <dd>

Bewirkt, dass alle Qualifizierer (einschließlich **Key** und **Dynamic**) im Vergleich ignoriert werden.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource** (2 (0x2))


</dt> <dd>

Bewirkt, dass die Quelle der Objekte, d. h. der Server und der Namespace, von dem sie stammen, im Vergleich zu anderen Objekten ignoriert wird.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues** (4 (0x4))


</dt> <dd>

Bewirkt, dass die Standardwerte von Eigenschaften ignoriert werden. Dieses Flag ist nur beim Vergleichen von Klassen sinnvoll.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass** (8 (0x8))


</dt> <dd>

Weist das System an, davon auszugehen, dass die verglichenen Objekte Instanzen derselben Klasse sind. Folglich vergleicht dieses Flag nur instanzbezogene Informationen. Mithilfe dieses Flags können Sie die Leistung optimieren. Wenn die Objekte nicht zu derselben Klasse gehören, sind die Ergebnisse undefiniert.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase** (16 (0x10))


</dt> <dd>

Bewirkt, dass Zeichenfolgenwerte ohne Unterscheidung nach Groß-/Kleinschreibung verglichen werden. Dies gilt sowohl für Zeichenfolgen als auch für Qualifiziererwerte. Unabhängig davon, ob dieses Flag angegeben ist, werden Eigenschaften- und Qualifizierernamen immer ohne Berücksichtigung von Groß- und Kleinschreibung verglichen.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor** (32 (0x20))


</dt> <dd>

Bewirkt, dass Qualifizierer-Varianten ignoriert werden. Dieses Flag berücksichtigt Qualifiziererwerte, ignoriert jedoch Unterschiede bei den verschiedenen Typen, z. B. Weitergaberegeln und Einschränkungen beim Überschreiben.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **CompareTo-Methode \_** gibt den booleschen Wert TRUE **zurück,** wenn die Objekte übereinstimmen. Andernfalls wird FALSE **zurückgegeben.**

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **CompareTo-Methode \_** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

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

Nicht genügend Arbeitsspeicher zum Abschließen des Vorgangs.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SWbemLastError**](swbemlasterror.md)
</dt> <dt>

[**Swbemobject**](swbemobject.md)
</dt> </dl>

 

 




