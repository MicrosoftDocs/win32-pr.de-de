---
description: Stellt Informationen zu den IQueryAssociations-Schnittstellenmethoden bereit.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: ASSOCF-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d52de3ce181033358fc20ca3e4f8759b61f72ed
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786696"
---
# <a name="assocf-enumeration"></a>ASSOCF-Enumeration

Stellt Informationen zu den [**IQueryAssociations-Schnittstellenmethoden**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) bereit.

## <a name="syntax"></a>Syntax




| C++ | 
|-----|
| <pre><code>typedef enum  {   ASSOCF_NONE                  = 0x00000000,  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,  ASSOCF_INIT_BYEXENAME        = 0x00000002,  ASSOCF_OPEN_BYEXENAME        = 0x00000002,  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,  ASSOCF_NOUSERSETTINGS        = 0x00000010,  ASSOCF_NOTRUNCATE            = 0x00000020,  ASSOCF_VERIFY                = 0x00000040,  ASSOCF_REMAPRUNDLL           = 0x00000080,  ASSOCF_NOFIXUPS              = 0x00000100,  ASSOCF_IGNOREBASECLASS       = 0x00000200,  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,  ASSOCF_IS_PROTOCOL           = 0x00001000,  ASSOCF_INIT_FOR_FILE         = 0x00002000} ASSOCF;</code></pre> | 




## <a name="constants"></a>Konstanten

 <span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF \_ NONE** 

Keine der folgenden Optionen ist festgelegt.

 <span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF \_ INIT \_ NOREMAPCLSID** 

Weist [**IQueryAssociations-Schnittstellenmethoden**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) an, KEINE CLSID-Werte ProgID-Werten zu zuordnen.

 <span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF \_ INIT \_ BYEXENAME** 

Identifiziert den Wert des *pwszAssoc-Parameters* [**von IQueryAssociations::Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) als ausführbaren Dateinamen. Wenn dieses Flag nicht festgelegt ist, wird der Stammschlüssel auf  die ProgID festgelegt, die dem.exe-Schlüssel anstelle der ProgID der ausführbaren Datei zugeordnet ist.

 <span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF \_ OPEN \_ BYEXENAME** 

Identisch mit **ASSOCF \_ INIT \_ BYEXENAME**.

 <span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF \_ INIT \_ DEFAULTTOSTAR** 

Gibt an, dass eine [**IQueryAssociations-Methode**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) versuchen soll, den vergleichbaren Wert aus dem Unterschlüssel abzurufen, wenn sie den angeforderten Wert unter dem Stammschlüssel **\*** nicht findet.

 <span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF \_ INIT \_ DEFAULTTOFOLDER** 

Gibt an, dass eine [**IQueryAssociations-Methode,**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) wenn sie den angeforderten Wert nicht unter dem Stammschlüssel findet, versuchen sollte, den vergleichbaren Wert aus dem **Ordnerunterschlüssel** abzurufen.

 <span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF \_ NOUSERSETTINGS** 

Gibt an, dass nur **HKEY \_ CLASSES \_ ROOT** durchsucht und **HKEY \_ CURRENT \_ USER** ignoriert werden soll.

 <span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF \_ NOTRUNCATE** 

Gibt an, dass die Rückgabezeichenfolge nicht abgeschnitten werden soll. Geben Sie stattdessen einen Fehlerwert und die erforderliche Größe für die vollständige Zeichenfolge zurück.

 <span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**ASSOCF \_ VERIFY** 

Weist [**IQueryAssociations-Methoden**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) an, zu überprüfen, ob die Daten korrekt sind. Mit dieser Einstellung können **IQueryAssociations-Methoden** Daten zur Überprüfung von der Festplatte des Benutzers lesen. Beispielsweise können sie den Benutzernamen in der Registrierung mit dem namen überprüfen, der in der .exe ist. Das Festlegen dieses Flags verringert in der Regel die Effizienz der -Methode.

 <span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF \_ REMAPRUNDLL** 

Weist [**IQueryAssociations-Methoden**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) an, Rundll.exe zu ignorieren und Informationen über das Ziel zurück zu geben. **IQueryAssociations-Methoden** geben in der Regel Informationen zum ersten .exe oder .dll in einer Befehlszeichenfolge zurück. Wenn ein Befehl Rundll.exe, weist das Festlegen dieses Flags die Methode an, Rundll.exe zu ignorieren und Informationen über das Ziel zurück zu geben.

 <span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF \_ NOFIXUPS** 

Weist [**IQueryAssociations-Methoden**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) an, Fehler in der Registrierung nicht zu beheben, z. B. der Angezeigte Name einer Funktion, die nicht mit dem in der .exe übereinstimmen.

 <span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF \_ IGNOREBASECLASS** 

Gibt an, dass der BaseClass-Wert ignoriert werden soll.

 <span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF \_ INIT \_ IGNOREUNKNOWN** 

**Eingeführt in Windows 7**. Gibt an, dass die ProgID "Unknown" ignoriert werden soll. führen Sie stattdessen zu einem Fehler.

 <span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**ASSOCF \_ INIT \_ FIXED \_ PROGID** 

**Eingeführt in Windows 8**. Gibt an, dass die angegebene ProgID mit den Systemeinstellungen und nicht mit den Standardeinstellungen des aktuellen Benutzers zugeordnet werden soll.

 <span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF \_ IS \_ PROTOCOL** 

**Eingeführt in Windows 8**. Gibt an, dass es sich bei dem Wert um ein Protokoll handelt, das mit den Standardwerten des aktuellen Benutzers zugeordnet werden soll.

 <span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF \_ INIT \_ FÜR \_ FILE** 

**Eingeführt in Windows 8.1**. Gibt an, dass die ProgID einer Dateierweiterungsbasierten Zuordnung entspricht. Verwenden Sie zusammen **mit ASSOCF \_ INIT \_ FIXED \_ PROGID**.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]               |
| Unterstützte Mindestversion (Server) | Windows 2000 Server \[nur Desktop-Apps\]                                 |
| Header                   |  Shlwapi.h  |



## <a name="see-also"></a>Siehe auch

 [**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) 

 

 

© 2017 Microsoft. Alle Rechte vorbehalten.
