---
description: Die CompareTo- \_ Methode des "errbemlasterror"-Objekts vergleicht zwei "errbeapbject"-Objekte. Dieser Vergleich unterliegt bestimmten Einschränkungen basierend auf den Werten, die im IFlags-Parameter angegeben sind.
ms.assetid: 541510e4-ef8d-4436-966f-19c5df422281
ms.tgt_platform: multiple
title: SWbemLastError.CompareTo_-Methode (wbemdisp. h)
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
ms.openlocfilehash: 4c24eb6e57e81c6c44922b2d6643be65198951ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347066"
---
# <a name="swbemlasterrorcompareto_-method"></a>Methode ' Swap. CompareTo ' \_

Die **CompareTo \_** -Methode des " [**errbemlasterror**](swbemlasterror.md) "-Objekts vergleicht zwei " [**errbeapbject**](swbemobject.md) "-Objekte. Dieser Vergleich unterliegt bestimmten Einschränkungen basierend auf den Werten, die im *IFlags* -Parameter angegeben sind.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objwbemujekt* \[ in\]
</dt> <dd>

Erforderlich. Ein-Objekt der Klasse " [**Swap**](swbemobject.md) -Klasse". Dieser Parameter ist das Objekt, mit dem das erste Objekt verglichen wird. Das Objekt muss eine gültige Instanz von " **errbemubject** " sein.

</dd> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Eine ganze Zahl, die zusätzliche Flags für den Vorgang angibt. Dieser Parameter gibt die Objekteigenschaften an, die bei der Objekt Vergleiche berücksichtigt werden müssen. Mit **wbemcomparisonflagincludeall** können Sie alle Features (Standard) oder eine beliebige Kombination der folgenden Werte in Erwägung gezogen.

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemcomparisonflagincluentall * * * * (0 (0x0))


</dt> <dd>

Bewirkt, dass alle Eigenschaften, Qualifizierer und Variationen verglichen werden.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemcomparisonflagignorequalifizierer * * * * (1 (0x1))


</dt> <dd>

Bewirkt, dass alle Qualifizierer (einschließlich **Key** und **Dynamic**) im Vergleich ignoriert werden.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemcomparisonflagignoreobjectsource * * * * (2 (0x2))


</dt> <dd>

Bewirkt, dass die Quelle der Objekte, nämlich der Server und der Namespace, von denen Sie stammen, im Vergleich zu anderen Objekten ignoriert werden.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemcomparisonflagignoredefaultvalues * * * * (4 (0x4))


</dt> <dd>

Bewirkt, dass die Standardwerte von Eigenschaften ignoriert werden. Dieses Flag ist nur beim Vergleich von Klassen sinnvoll.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemcomparisonflagignoreclass * * * * (8 (0x8))


</dt> <dd>

Weist das System an, davon auszugehen, dass es sich bei den verglichenen Objekten um Instanzen derselben Klasse handelt. Folglich vergleicht dieses Flag nur instanzbezogene Informationen. Mithilfe dieses Flags können Sie die Leistung optimieren. Wenn die Objekte nicht zu derselben Klasse gehören, sind die Ergebnisse undefiniert.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemcomparisonflagignorecase * * * * (16 (0x10))


</dt> <dd>

Bewirkt, dass Zeichen folgen Werte ohne Beachtung der Groß-/Kleinschreibung verglichen werden. Dies gilt sowohl für Zeichen folgen als auch für Qualifiziererwerte. Unabhängig davon, ob dieses Flag angegeben ist, werden Eigenschaften- und Qualifizierernamen immer ohne Berücksichtigung von Groß- und Kleinschreibung verglichen.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemcomparisonflagignoreflavor * * * * (32 (0x20))


</dt> <dd>

Bewirkt, dass qualifizierervarianten ignoriert werden. Dieses Flag berücksichtigt Qualifiziererwerte, ignoriert jedoch Unterschiede bei den verschiedenen Typen, z. B. Weitergaberegeln und Einschränkungen beim Überschreiben.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **CompareTo \_** -Methode gibt den booleschen Wert **true** zurück, wenn die Objekte entsprechen; andernfalls wird **false** zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **CompareTo \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Austausch Fehler**](swbemlasterror.md)
</dt> <dt>

[**Austausch Objekt**](swbemobject.md)
</dt> </dl>

 

 




