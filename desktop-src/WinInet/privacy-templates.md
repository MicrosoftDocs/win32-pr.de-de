---
title: Datenschutzvorlagen (Wininet.h)
description: Die folgenden Datenschutzebenen entsprechen Regeln zum Akzeptieren, bedingten Akzeptieren oder Nicht akzeptieren von Cookies.
ms.assetid: d8dd9c12-b159-4f95-820e-521aeb1526bf
topic_type:
- apiref
api_name:
- PRIVACY_TEMPLATE_NO_COOKIES
- PRIVACY_TEMPLATE_HIGH
- PRIVACY_TEMPLATE_MEDIUM_HIGH
- PRIVACY_TEMPLATE_MEDIUM
- PRIVACY_TEMPLATE_MEDIUM_LOW
- PRIVACY_TEMPLATE_LOW
- PRIVACY_TEMPLATE_CUSTOM
- PRIVACY_TEMPLATE_ADVANCED
- PRIVACY_TEMPLATE_MAX
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481aa3e9b6b5b5519bac6e458de1acba90f2cfa20dd0a5babac016d0003c70b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955560"
---
# <a name="privacy-templates"></a>Datenschutzvorlagen

Die folgenden Datenschutzebenen entsprechen Regeln zum Akzeptieren, bedingten Akzeptieren oder Nicht akzeptieren von Cookies. Diese Ebenen entsprechen den Datenschutzpräferenzebenen, die auf der Registerkarte Datenschutz unter Internetoptionen festgelegt sind. Ausführliche Definitionen finden Sie [unter Datenschutz in Internet Explorer 6.](https://www.bing.com/search?q=Privacy+in+Internet+Explorer+6)

<dl> <dt>

<span id="PRIVACY_TEMPLATE_NO_COOKIES"></span><span id="privacy_template_no_cookies"></span>**DATENSCHUTZVORLAGE \_ \_ KEINE \_ COOKIES**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Dies entspricht dem Schieberegler **Alle Cookies blockieren** auf der Schiebeleiste Datenschutzeinstellungen unter **Internetoptionen**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_HIGH"></span><span id="privacy_template_high"></span>**DATENSCHUTZVORLAGE \_ \_ HOCH**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Dies ist identisch mit **Hoch** auf der Schiebereglerleiste Datenschutzeinstellungen unter **Internetoptionen**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_HIGH"></span><span id="privacy_template_medium_high"></span>**DATENSCHUTZVORLAGE \_ \_ MITTEL \_ HOCH**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Dies ist identisch mit **Mittel \_ hoch** auf der Schiebereglerleiste Datenschutzeinstellungen unter **Internetoptionen**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM"></span><span id="privacy_template_medium"></span>**MEDIUM \_ DER DATENSCHUTZVORLAGE \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Dies ist identisch mit **Medium** auf der Schiebereglerleiste Datenschutzeinstellungen unter **Internetoptionen**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_LOW_"></span><span id="privacy_template_medium_low_"></span>**DATENSCHUTZVORLAGE \_ \_ MITTEL \_ NIEDRIG** 
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Dies ist identisch mit **Niedrig** auf der Schiebereglerleiste Datenschutzeinstellungen unter **Internetoptionen**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_LOW"></span><span id="privacy_template_low"></span>**DATENSCHUTZVORLAGE \_ \_ NIEDRIG**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Dies entspricht dem Schieberegler **Alle Cookies akzeptieren** auf der Schiebeleiste Datenschutzeinstellungen unter **Internetoptionen.**


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_CUSTOM"></span><span id="privacy_template_custom"></span>**BENUTZERDEFINIERTE \_ DATENSCHUTZVORLAGE \_**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



Benutzerdefiniert. Unter [How to Create a Customized Privacy Import File (Erstellen einer benutzerdefinierten Datenschutzimportdatei)](https://www.bing.com/search?q=How+to+Create+a+Customized+Privacy+Import+File) erfahren Sie, wie Sie benutzerdefinierte Datenschutzeinstellungen festlegen.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_ADVANCED"></span><span id="privacy_template_advanced"></span>**DATENSCHUTZVORLAGE \_ \_ ERWEITERT**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Benutzerdefiniert. Erweiterte Optionen werden im Dialogfeld **Erweiterter Datenschutz Einstellungen** festgelegt, das über die Registerkarte **Datenschutz** unter **Internetoptionen** erreichbar ist.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MAX"></span><span id="privacy_template_max"></span>**\_MAX. DATENSCHUTZVORLAGE \_**
</dt> <dd> <dl> <dt>

DATENSCHUTZVORLAGE \_ \_ NIEDRIG
</dt> <dt>



Entspricht **der \_ DATENSCHUTZVORLAGE \_ LOW**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

> [!Note]  
> WinINet unterstützt keine Serverimplementierungen. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP-Dienste (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wininet.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PrivacyGetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**PrivacySetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

