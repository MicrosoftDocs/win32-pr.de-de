---
description: Dieser Abschnitt enthält das Referenzmaterial zum Portieren der veralteten Win32-APIs für mobiles Breitband in die entsprechenden Windows Runtime-APIs.
title: Richtlinien für das Portieren mobiler Breitband-Win32-APIs zu Windows Runtime-APIs
ms.topic: reference
ms.date: 08/23/2021
ms.openlocfilehash: 4cbe0415e40f18d372fdd8b9089dbd4afe197b38
ms.sourcegitcommit: 8d7ce0c4827f8a4fd501cc6487f1a8360e944577
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2021
ms.locfileid: "122767709"
---
# <a name="guidelines-for-porting-mobile-broadband-win32-apis-to-windows-runtime-apis"></a>Richtlinien für das Portieren mobiler Breitband-Win32-APIs zu Windows Runtime-APIs

In dieser Tabelle sind die entsprechenden Windows Runtimefunktionen für die veralteten Win32-APIs für mobiles Breitband aufgeführt.

| **IMbnConnection** |  Äquivalente Windows Runtime-Funktionalität |
| - | - |
| Verbinden | ConnectivityManager.AcquireConnectionAsync |
| Trennen | ConnectionSession.Close |
| Get \_ InterfaceID | MobileBroadbandAccount.NetworkAccountId |
| GetActivationNetworkError | MobileBroadbandNetwork.ActivationNetworkError |
| GetConnectionState | WwanConnectionProfileDetails.GetNetworkRegistrationState |
| GetVoiceCallState | MobileBroadbandNetwork.GetVoiceCallSupport, PhoneCallManager.IsCallActive |
| **IMbnConnectionEvents** | |
| OnConnectComplete | NetworkStateChangeEventDetails.HasNewWwanRegistrationState: Nach der Benachrichtigung kann der aktuelle Registrierungsstatus aus WwanConnectionProfileDetails.GetNetworkRegistrationState abgerufen werden. |
| OnConnectStateChange | NetworkStateChangeEventDetails.HasNewWwanRegistrationState: Nach der Benachrichtigung kann der aktuelle Registrierungsstatus aus WwanConnectionProfileDetails.GetNetworkRegistrationState abgerufen werden. |
| OnDisconnectComplete | NetworkStateChangeEventDetails.HasNewWwanRegistrationState: Nach der Benachrichtigung kann der aktuelle Registrierungsstatus aus WwanConnectionProfileDetails.GetNetworkRegistrationState abgerufen werden. |
| OnVoiceCallStateChange | PhoneCallManager.CallStateChanged |
| **IMbnConnectionProfile** | |
| Löschen | ConnectionProfile.TryDeleteAsync |
| GetConnectionProfile | NetworkAdapter.GetConnectedProfileAsync |
| GetConnectionProfiles | NetworkInformation.GetConnectionProfiles |
| **IMbnDeviceService** | |
| CloseCommandSession | MobileBroadbandDeviceServiceCommandSession.CloseSession |
| CloseDataSession | MobileBroadbandDeviceServiceDataSession.CloseSession |
| Abrufen von \_ DeviceServiceID | MobileBroadbandDeviceService.DeviceServiceId |
| OpenCommandSession | MobileBroadbandDeviceService.OpenCommandSession |
| OpenDataSession | MobileBroadbandDeviceService.OpenDataSession |
| QueryCommand | MobileBroadbandDeviceServiceCommandSession.SendQueryCommandAsync |
| QuerySupportedCommands | MobileBroadbandDeviceService.SupportedCommands |
| SetCommand | MobileBroadbandDeviceServiceCommandSession.SendSetCommandAsync |
| WriteData | MobileBroadbandDeviceServiceDataSession.WriteDataAsync |
| **IMbnDeviceServicesContext** | |
| EnumerateDeviceServices | MobileBroadbandDeviceService.SupportedCommands |
| get \_ MaxCommandSize | MobileBroadbandModem.MaxDeviceServiceCommandSizeInBytes |
| \_MaxDataSize abrufen | MobileBroadbandModem.MaxDeviceServiceDataSizeInByte |
| GetDeviceService | MobileBroadbandModem.GetDeviceService |
| **IMbnDeviceServicesEvents** | |
| OnReadData | MobileBroadbandDeviceServiceDataSession.DataReceived |
| **IMbnInterface** | |
| Get \_ InterfaceID | MobileBroadbandAccount.NetworkAccountId |
| GetConnection | Von AcquireConnectionAsync abgerufene ConnectionSession |
| GetHomeProvider | MobileBroadbandModem.GetCurrentConfigurationAsync |
| GetInterfaceCapability | MobileBroadbandAccount.CurrentDeviceInformation |
| GetReadyState | MobileBroadbandDeviceInformation.NetworkDeviceStatus |
| GetSubscriberInformation | MobileBroadbandAccount.CurrentDeviceInformation |
| InEmergencyMode | MobileBroadbandModem.IsInEmergencyCallMode |
| **IMbnInterfaceEvents** | |
| OnEmergencyModeChange | MobileBroadbandModem.IsInEmergencyCallModeChanged |
| OnReadyStateChange | MobileBroadbandNetworkRegistrationStateChange |
| OnSubscriberInformationChange | MobileBroadbandAccountUpdatedEventArgs.HasDeviceInformationChanged |
| **IMbnInterfaceManager** | |
| Getinterface | MobileBroadbandModem.CurrentAccount |
| **IMbnInterfaceManagerEvents** | |
| OnInterface Ausschn. | MobileBroadbandAccountWatcher.AccountAdded |
| OnInterfaceRemoval | MobileBroadbandAccountWatcher.Account |
| **IMbnMultiCarrier** | |
| GetCurrentCellularClass | MobileBroadbandDeviceInformation.CellularClass |
| **IMbnMultiCarrierEvents** | |
| OnCurrentCellularClassChange | MobileBroadbandAccountUpdatedEventArgs.HasDeviceInformationChanged |
| **IMbnPin** | |
| Change | MobileBroadbandPin.ChangeAsync |
| Disable | MobileBroadbandPin.DisableAsync |
| Aktivieren | MobileBroadbandPin.EnableAsync |
| EINGABETASTE | MobileBroadbandPin.EnterAsync |
| PinFormat abrufen \_ | MobileBroadbandPin.Format |
| \_PinLengthMax abrufen | MobileBroadbandPin.MaxLength |
| get \_ PinLengthMin | MobileBroadbandPin.MaxLength |
| Get \_ PinMode | MobileBroadbandPin.Enabled |
| \_PinType abrufen | MobileBroadbandPin.Type |
| GetPinManager | MobileBroadbandDeviceInformation.PinManager |
| Entsperren | MobileBroadbandPin.UnblockAsync |
| **IMbnPinManager** | |
| GetPin | MobileBroadbandPinManager.GetPin |
| GetPinList | MobileBroadbandPinManager.SupportedPins |
| GetPinState | MobileBroadbandPin.LockState |
| **IMbnPinManagerEvents** | |
| **IMbnRadio** | |
| Get \_ SoftwareRadioState | Radio.GetRadiosAsync – Radio. State |
| SetSoftwareRadioState | Radio.SetStateAsync |
| **IMbnRadioEvents** | |
| OnRadioStateChange | Radio.StateChanged |
| **IMbnRegistration** | |
| GetAvailableDataClasses | MobileBroadbandDeviceInformation.DataClasses |
| GetCurrentDataClass | MobileBroadbandNetwork.RegisteredDataClass |
| GetPacketAttachNetworkError | MobileBroadbandNetwork.PacketAttachNetworkError |
| GetProviderID | MobileBroadbandNetwork.RegisteredProviderId |
| GetProviderName | MobileBroadbandNetwork.RegisteredProviderName |
| GetRegisterState | MobileBroadbandNetwork.NetworkRegistrationState |
| GetRegistrationNetworkError | MobileBroadbandNetwork.ActivationNetworkError |
| **IMbnRegistrationEvents** | |
| OnPacketServiceStateChange | MobileBroadbandNetworkRegistrationStateChange |
| OnRegisterStateChange | MobileBroadbandNetworkRegistrationStateChange |
| GetSignalStrength | ConnectionProfile.GetSignalBar / MobileBroadbandCellLte.ReferenceSignalReceivedPowerInDBm / MobileBroadbandCellGsm.ReceivedSignalStrengthInDBm |
| **IMbnSignalEvents** | |
| **IMbnSms** | |
| GetSmsConfiguration | SmsDevice2.SmscAddress, SmsDevice2.CellularClass, None für CDMAShortMessageSize und MaxMessageIndex, was nicht als öffentliche API erforderlich ist. |
| SetSmsConfiguration | SmsDevice2.SmscAddress, keiner der anderen Parameter wird unterstützt. |
| SmsSendCdma | SendMessageAndGetResultAsync mithilfe von CellularClass in ISmsMessageBase |
| SmsSendCdmaPdu | SendMessageAndGetResultAsync mit Messagetype und CellularClass in ISmsMessageBase |
| SmsSendPdu | SendMessageAndGetResultAsync mit MessageType in ISmsMessageBase |
| **IMbnSmsConfiguration** | |
| \_ServiceCenterAddress abrufen | SmsDevice2.SmscAddress |
| get \_ SmsFormat | SmsDevice2.CellularClass |
| \_put ServiceCenterAddress | SmsDevice2.SmscAddress |
| **IMbnSmsEvents** | |
| OnSmsNewClass0Message | SmsMessageRegistration.MessageReceived |
| OnSmsSendComplete | SmsSendMessageResult |
| **IMbnSmsReadMsgPdu** | |
| get \_ Message | SmsTextMessage2.Body |
| Abrufen \_ von PduData | SmsTextmessage2.Body |
| **IMbnSmsReadMsgTextCdma** | |
| get \_ Address (Adresse abrufen) | SmsTextMessage2.From |
| get \_ EncodingID | SmsTextMessage2.Encoding |
| get \_ Message | SmsTextMessage2.Body |
| Get \_ Timestamp | SmsTextMessage.2Timestamp |
| **IMbnSubscriberInformation** | |
| Get \_ SimIccID | MobileBroadbandDeviceInformation.SimIccId |
| Get \_ SubscriberID | MobileBroadbandDeviceInformation.SubscriberId |
| get \_ TelephoneNumbers | MobileBroadbandDeviceInformation.TelephoneNumbers |
